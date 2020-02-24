---
title: Integravimo su „Dayforce “ konfigūravimas
description: Integravimas tarp „Microsoft Dynamics 365 Human Resources“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šiame straipsnyje. Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Human Resources“, tiek „Dayforce“.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85e7274b0e9c130e5c3426fd1fff98410f93e49a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009894"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="0ce93-104">Integravimo su „Dayforce “ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="0ce93-105">Integravimas tarp „Microsoft Dynamics 365 Human Resources“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šiame straipsnyje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="0ce93-106">Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Human Resources“, tiek „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="0ce93-107">Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="0ce93-108">Integravimui reikalingi konkretūs duomenys iš „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="0ce93-109">Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Human Resources“ taip, kad integravimas būtų palaikomas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="0ce93-110">Integravimui naudojamos šios plačios duomenų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="0ce93-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="0ce93-111">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="0ce93-111">Human resources data</span></span>
- <span data-ttu-id="0ce93-112">Kompensacijos duomenys</span><span class="sxs-lookup"><span data-stu-id="0ce93-112">Compensation data</span></span>
- <span data-ttu-id="0ce93-113">Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="0ce93-114">Darbuotojo duomenys</span><span class="sxs-lookup"><span data-stu-id="0ce93-114">Worker data</span></span>

<span data-ttu-id="0ce93-115">Šiame straipsnyje aprašomi veiksmai, kuriuos reikia vykdyti norint įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="0ce93-116">Joje taip pat paaiškinami duomenų tipai ir išsami konfigūravimo informacija, reikalinga integravimui.</span><span class="sxs-lookup"><span data-stu-id="0ce93-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="0ce93-117">Integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-117">Enable the integration</span></span>

<span data-ttu-id="0ce93-118">Pirmiausia programoje „Human Resources“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="0ce93-119">Jei norite, kad sukuriama didžiosios knygos operacija būtų importuota į „Microsoft Dynamics 365 Finance“, taip pat turite sukurti „Microsoft Azure“ saugyklos paskyrą ir įvesti „Azure Storage“ jungimosi eilutę į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="0ce93-120">Norėdami įjungti integravimą į „Human Resources“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0ce93-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="0ce93-121">Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="0ce93-122">Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.</span><span class="sxs-lookup"><span data-stu-id="0ce93-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="0ce93-123">Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.</span><span class="sxs-lookup"><span data-stu-id="0ce93-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="0ce93-124">Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="0ce93-125">Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="0ce93-126">Galite pakeisti šį dažnumą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="0ce93-127">Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="0ce93-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="0ce93-128">Apie „Azure“ saugyklos paskyras</span><span class="sxs-lookup"><span data-stu-id="0ce93-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="0ce93-129">„Azure Storage“ jungimosi eilučių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="0ce93-130">Techninė informacija apie algalapių integravimo įjungimą</span><span class="sxs-lookup"><span data-stu-id="0ce93-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="0ce93-131">Įjungus algalapių integravimą gaunami du pagrindiniai rezultatai:</span><span class="sxs-lookup"><span data-stu-id="0ce93-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="0ce93-132">Sukuriamas duomenų eksportavimo projektas pavadinimu Atlyginimų integravimo eksportavimas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="0ce93-133">Šiame projekte yra objektai ir laukai, kurie būtini norint užtikrinti algalapių integravimą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="0ce93-134">Norėdami analizuoti projektą, eikite į **Sistemos administravimas**, pasirinkite plytelę **Duomenų valdymas**, tada projektų sąraše atidarykite duomenų projektą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="0ce93-135">Ši paketinė užduotis vykdo duomenų eksportavimo projektą, užšifruoja gautą duomenų paketą ir perduoda duomenų paketo failą į SFTP galinį punktą, sukonfigūruotą ekrane **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="0ce93-136">Duomenų paketas, perduotas į SFTP galinį punktą, užšifruojamas naudojant unikalų pakuotės raktą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="0ce93-137">Raktas laikomas „Azure Key Vault“, kurį gali pasiekti tik „Ceridian“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="0ce93-138">Neįmanoma iššifruoti ir išanalizuoti duomenų paketo turinio.</span><span class="sxs-lookup"><span data-stu-id="0ce93-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="0ce93-139">Jei reikia analizuoti duomenų paketo turinį, reikės rankiniu būdu eksportuoti duomenų projektą Atlyginimų integravimo eksportavimas, jį atsisiųsti ir tada atsidaryti.</span><span class="sxs-lookup"><span data-stu-id="0ce93-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="0ce93-140">Eksportuojant rankiniu būdu nebus taikomas šifravimas ir paketas nebus perduodamas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="0ce93-141">Jūsų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-141">Configure your data</span></span> 

<span data-ttu-id="0ce93-142">Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="0ce93-143">Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir kompensacijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="0ce93-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="0ce93-144">Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="0ce93-145">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="0ce93-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="0ce93-146">Išmokos</span><span class="sxs-lookup"><span data-stu-id="0ce93-146">Benefits</span></span> 

<span data-ttu-id="0ce93-147">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų kompensacijų planus.</span><span class="sxs-lookup"><span data-stu-id="0ce93-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="0ce93-148">Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="0ce93-149">Išmokų planai</span><span class="sxs-lookup"><span data-stu-id="0ce93-149">Benefit plans</span></span>

- <span data-ttu-id="0ce93-150">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-150">Plan (required)</span></span>
- <span data-ttu-id="0ce93-151">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-151">Type (required)</span></span>
- <span data-ttu-id="0ce93-152">Poveikis algalapiui (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-152">Payroll impact (required)</span></span>
- <span data-ttu-id="0ce93-153">Susigrąžinti skolas</span><span class="sxs-lookup"><span data-stu-id="0ce93-153">Recover arrears</span></span>
- <span data-ttu-id="0ce93-154">Atskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-154">Deduction method</span></span>
- <span data-ttu-id="0ce93-155">Atskaitymo pirmumas</span><span class="sxs-lookup"><span data-stu-id="0ce93-155">Deduction priority</span></span>
- <span data-ttu-id="0ce93-156">Apribojimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="0ce93-156">Limit period</span></span>
- <span data-ttu-id="0ce93-157">Limito suma</span><span class="sxs-lookup"><span data-stu-id="0ce93-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="0ce93-158">Išmokos</span><span class="sxs-lookup"><span data-stu-id="0ce93-158">Benefits</span></span>

- <span data-ttu-id="0ce93-159">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-159">Plan (required)</span></span>
- <span data-ttu-id="0ce93-160">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-160">Type (required)</span></span>
- <span data-ttu-id="0ce93-161">Parinktis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-161">Option (required)</span></span>
- <span data-ttu-id="0ce93-162">Išmokos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-162">Benefit ID (required)</span></span>
- <span data-ttu-id="0ce93-163">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="0ce93-163">Frequency</span></span>
- <span data-ttu-id="0ce93-164">Pagrindas</span><span class="sxs-lookup"><span data-stu-id="0ce93-164">Basis</span></span>
- <span data-ttu-id="0ce93-165">Suma arba tarifas</span><span class="sxs-lookup"><span data-stu-id="0ce93-165">Amount or rate</span></span>
- <span data-ttu-id="0ce93-166">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="0ce93-167">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="0ce93-167">Supported frequencies</span></span> 

- <span data-ttu-id="0ce93-168">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-168">Weekly</span></span>
- <span data-ttu-id="0ce93-169">Už dvi savaites</span><span class="sxs-lookup"><span data-stu-id="0ce93-169">Bi-weekly</span></span>
- <span data-ttu-id="0ce93-170">Kas pusę mėnesio</span><span class="sxs-lookup"><span data-stu-id="0ce93-170">Semi-monthly</span></span>
- <span data-ttu-id="0ce93-171">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="0ce93-172">Palaikomos bazės</span><span class="sxs-lookup"><span data-stu-id="0ce93-172">Supported bases</span></span> 

- <span data-ttu-id="0ce93-173">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="0ce93-173">Fixed amount</span></span>
- <span data-ttu-id="0ce93-174">Pajamų procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="0ce93-174">Percent of earnings</span></span>
- <span data-ttu-id="0ce93-175">Produktyvios valandos</span><span class="sxs-lookup"><span data-stu-id="0ce93-175">Productive hours</span></span>

<span data-ttu-id="0ce93-176">„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.</span><span class="sxs-lookup"><span data-stu-id="0ce93-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="0ce93-177">Pasirinkimas programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="0ce93-177">Selection in Human Resources</span></span>        | <span data-ttu-id="0ce93-178">Rezultatas „Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0ce93-179">Jokia</span><span class="sxs-lookup"><span data-stu-id="0ce93-179">None</span></span>                       | <span data-ttu-id="0ce93-180">Nesukuriama jokio atskaitymo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="0ce93-181">Tik atskaitymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-181">Deduction only</span></span>             | <span data-ttu-id="0ce93-182">Sukuriamas darbuotojo atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="0ce93-183">Tik įnašas</span><span class="sxs-lookup"><span data-stu-id="0ce93-183">Contribution only</span></span>          | <span data-ttu-id="0ce93-184">Sukuriamas darbdavio atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="0ce93-185">Atskaitymas ir įnašas</span><span class="sxs-lookup"><span data-stu-id="0ce93-185">Deduction and contribution</span></span> | <span data-ttu-id="0ce93-186">Sukuriami darbuotojo ir darbdavio atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="0ce93-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="0ce93-187">Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="0ce93-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="0ce93-188">Darbuotojų išmokų programos teikimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="0ce93-189">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="0ce93-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="0ce93-190">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="0ce93-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="0ce93-191">Užregistruoti ir pašalinti išmokas darbuotojams</span><span class="sxs-lookup"><span data-stu-id="0ce93-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="0ce93-192">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-192">Compensation</span></span> 

<span data-ttu-id="0ce93-193">Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="0ce93-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="0ce93-194">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="0ce93-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="0ce93-195">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="0ce93-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="0ce93-196">„Dayforce“ naudojama kompensacijos informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="0ce93-197">Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="0ce93-198">Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.</span><span class="sxs-lookup"><span data-stu-id="0ce93-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="0ce93-199">Daugiau informacijos apie kompensacijų planus rasite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="0ce93-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="0ce93-200">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="0ce93-201">Kintamosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="0ce93-202">Kurti atlyginimų / kompensavimo struktūrą ir planus</span><span class="sxs-lookup"><span data-stu-id="0ce93-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="0ce93-203">Kompensavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="0ce93-204">Kompensavimo proceso nustatymas ir rezultatų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="0ce93-205">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="0ce93-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="0ce93-206">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="0ce93-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="0ce93-207">Darbai</span><span class="sxs-lookup"><span data-stu-id="0ce93-207">Jobs</span></span> 

<span data-ttu-id="0ce93-208">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="0ce93-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="0ce93-209">Daugiau informacijos ieškokite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="0ce93-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="0ce93-210">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="0ce93-211">Naujų darbo vietų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="0ce93-212">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="0ce93-212">Positions</span></span>

<span data-ttu-id="0ce93-213">Pareigos yra atskiros užduoties egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="0ce93-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="0ce93-214">Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="0ce93-215">Pareigos egzistuoja padalinyje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-215">A position exists in a department.</span></span> <span data-ttu-id="0ce93-216">Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="0ce93-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="0ce93-217">Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:</span><span class="sxs-lookup"><span data-stu-id="0ce93-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="0ce93-218">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-218">Position (required)</span></span>
- <span data-ttu-id="0ce93-219">Aprašas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-219">Description (required)</span></span>
- <span data-ttu-id="0ce93-220">Užduotis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-220">Job (required)</span></span>
- <span data-ttu-id="0ce93-221">Padalinys (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-221">Department (required)</span></span>
- <span data-ttu-id="0ce93-222">Pareigų tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-222">Position type (required)</span></span>
- <span data-ttu-id="0ce93-223">Viso etato ekvivalentas</span><span class="sxs-lookup"><span data-stu-id="0ce93-223">Full-time equivalent</span></span>
- <span data-ttu-id="0ce93-224">Įprastos darbo valandos per metus (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="0ce93-225">Apmokama juridinio subjekto (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="0ce93-226">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-226">Pay cycle (required)</span></span>
- <span data-ttu-id="0ce93-227">Numatytosios finansinės dimensijos – išlaidų centras (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="0ce93-228">Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="0ce93-229">Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="0ce93-230">Daugiau informacijos ieškokite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="0ce93-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="0ce93-231">Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas</span><span class="sxs-lookup"><span data-stu-id="0ce93-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="0ce93-232">Pareigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="0ce93-233">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="0ce93-233">Departments</span></span>

<span data-ttu-id="0ce93-234">Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="0ce93-235">Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="0ce93-236">Padalinius galite naudoti norėdami pranešti apie funkcines sritis.</span><span class="sxs-lookup"><span data-stu-id="0ce93-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="0ce93-237">Padaliniai gali turėti pelno ir nuostolio atsakomybę.</span><span class="sxs-lookup"><span data-stu-id="0ce93-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="0ce93-238">Daugiau informacijos ieškokite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="0ce93-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="0ce93-239">Padalinio sukūrimas ir susiejimas su padalinių hierarchija</span><span class="sxs-lookup"><span data-stu-id="0ce93-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="0ce93-240">Apibrėžti naujus padalinius</span><span class="sxs-lookup"><span data-stu-id="0ce93-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="0ce93-241">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="0ce93-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="0ce93-242">Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams.</span><span class="sxs-lookup"><span data-stu-id="0ce93-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="0ce93-243">Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="0ce93-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="0ce93-244">Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="0ce93-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="0ce93-245">Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.</span><span class="sxs-lookup"><span data-stu-id="0ce93-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="0ce93-246">Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="0ce93-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="0ce93-247">Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="0ce93-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="0ce93-248">Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.</span><span class="sxs-lookup"><span data-stu-id="0ce93-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="0ce93-249">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="0ce93-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0ce93-250">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-250">Pay cycle (required)</span></span>
- <span data-ttu-id="0ce93-251">Mokėjimo ciklo dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="0ce93-252">Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="0ce93-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="0ce93-253">Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="0ce93-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="0ce93-254">Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui.</span><span class="sxs-lookup"><span data-stu-id="0ce93-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="0ce93-255">Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="0ce93-256">„Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="0ce93-257">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-257">Earning codes</span></span>

<span data-ttu-id="0ce93-258">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0ce93-259">Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="0ce93-260">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="0ce93-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0ce93-261">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-261">Earning Code (required)</span></span>
- <span data-ttu-id="0ce93-262">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-262">Description</span></span>
- <span data-ttu-id="0ce93-263">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="0ce93-263">Unit of measure</span></span>
- <span data-ttu-id="0ce93-264">Produktyvus</span><span class="sxs-lookup"><span data-stu-id="0ce93-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="0ce93-265">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="0ce93-265">Worker data</span></span>

<span data-ttu-id="0ce93-266">Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms.</span><span class="sxs-lookup"><span data-stu-id="0ce93-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="0ce93-267">Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.</span><span class="sxs-lookup"><span data-stu-id="0ce93-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="0ce93-268">Galite tvarkyti šią darbininkų informaciją:</span><span class="sxs-lookup"><span data-stu-id="0ce93-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="0ce93-269">**Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.</span><span class="sxs-lookup"><span data-stu-id="0ce93-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="0ce93-270">**Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="0ce93-271">**Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="0ce93-272">**Kompensacija ir algalapis** – tvarkykite informaciją apie darbininko kompensacijos planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.</span><span class="sxs-lookup"><span data-stu-id="0ce93-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="0ce93-273">Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="0ce93-274">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-274">General information</span></span>

- <span data-ttu-id="0ce93-275">Darbuotojo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-275">Personnel number (required)</span></span>
- <span data-ttu-id="0ce93-276">Vardas (būtinas)</span><span class="sxs-lookup"><span data-stu-id="0ce93-276">First name (required)</span></span>
- <span data-ttu-id="0ce93-277">Pavardė (būtinai)</span><span class="sxs-lookup"><span data-stu-id="0ce93-277">Last name (required)</span></span>
- <span data-ttu-id="0ce93-278">Antras vardas</span><span class="sxs-lookup"><span data-stu-id="0ce93-278">Middle name</span></span>
- <span data-ttu-id="0ce93-279">Paaukštinimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-279">Seniority date</span></span>
- <span data-ttu-id="0ce93-280">Žinoma kaip</span><span class="sxs-lookup"><span data-stu-id="0ce93-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="0ce93-281">Asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-281">Personal information</span></span>

- <span data-ttu-id="0ce93-282">Šeiminė padėtis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-282">Marital status (required)</span></span>
- <span data-ttu-id="0ce93-283">Gimimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-283">Birth date (required)</span></span>
- <span data-ttu-id="0ce93-284">Lytis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-284">Gender (required)</span></span>
- <span data-ttu-id="0ce93-285">Asmuo su negalia</span><span class="sxs-lookup"><span data-stu-id="0ce93-285">Person with disabilities</span></span>
- <span data-ttu-id="0ce93-286">Pilietybės šalies regionas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="0ce93-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="0ce93-287">Adresas</span><span class="sxs-lookup"><span data-stu-id="0ce93-287">Address information</span></span>

- <span data-ttu-id="0ce93-288">Pagrindinis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-288">Primary (required)</span></span>
- <span data-ttu-id="0ce93-289">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-289">Country/region (required)</span></span>
- <span data-ttu-id="0ce93-290">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-290">Postal code (required)</span></span>
- <span data-ttu-id="0ce93-291">Gatvės numeris (būtina) (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="0ce93-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="0ce93-292">Pastatų kompleksas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="0ce93-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="0ce93-293">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-293">City (required)</span></span>
- <span data-ttu-id="0ce93-294">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-294">State (required)</span></span>
- <span data-ttu-id="0ce93-295">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="0ce93-296">Kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-296">Contact information</span></span> 

- <span data-ttu-id="0ce93-297">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-297">Primary (required)</span></span>
- <span data-ttu-id="0ce93-298">Kontakto numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-298">Contact number (required)</span></span>
- <span data-ttu-id="0ce93-299">Išplėtimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="0ce93-300">Algalapio informacija ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-300">Payroll information and earning codes</span></span>

<span data-ttu-id="0ce93-301">Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="0ce93-302">Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.</span><span class="sxs-lookup"><span data-stu-id="0ce93-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="0ce93-303">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-303">Earning codes</span></span>

- <span data-ttu-id="0ce93-304">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-304">Position (required)</span></span>
- <span data-ttu-id="0ce93-305">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-305">Earning Code (required)</span></span>
- <span data-ttu-id="0ce93-306">Dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-306">Frequency (required)</span></span>
- <span data-ttu-id="0ce93-307">Suma (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="0ce93-308">Algalapių informacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-308">Payroll information</span></span>

- <span data-ttu-id="0ce93-309">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="0ce93-309">Payment Method</span></span>
- <span data-ttu-id="0ce93-310">Ekonominė sritis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-310">Economic Region (required)</span></span>
- <span data-ttu-id="0ce93-311">Darbuotojų išmokų ID</span><span class="sxs-lookup"><span data-stu-id="0ce93-311">Employee Benefits ID</span></span>
- <span data-ttu-id="0ce93-312">Asmens kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-312">National ID Number (required)</span></span>
- <span data-ttu-id="0ce93-313">Karo tarnybos numeris</span><span class="sxs-lookup"><span data-stu-id="0ce93-313">Military Service Number</span></span>
- <span data-ttu-id="0ce93-314">Pamainos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-314">Shift ID (required)</span></span>
- <span data-ttu-id="0ce93-315">Mokesčių numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-315">Tax Number (required)</span></span>
- <span data-ttu-id="0ce93-316">Sąjungos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-316">Union ID (required)</span></span>
- <span data-ttu-id="0ce93-317">Darbo dienos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-317">Work Day ID (required)</span></span>
- <span data-ttu-id="0ce93-318">Darbo leidimo numeris</span><span class="sxs-lookup"><span data-stu-id="0ce93-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="0ce93-319">Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="0ce93-320">Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="0ce93-321">Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-321">Employment details</span></span>

<span data-ttu-id="0ce93-322">Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos.</span><span class="sxs-lookup"><span data-stu-id="0ce93-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="0ce93-323">„Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="0ce93-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="0ce93-324">Įdarbinimo pradžios data (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-324">Employment start date (required)</span></span>
- <span data-ttu-id="0ce93-325">Įdarbinimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="0ce93-325">Employment end date</span></span>
- <span data-ttu-id="0ce93-326">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="0ce93-326">Start date</span></span>
- <span data-ttu-id="0ce93-327">Patikslinta darbo pradžios data</span><span class="sxs-lookup"><span data-stu-id="0ce93-327">Adjusted start date</span></span>
- <span data-ttu-id="0ce93-328">Atleidimo data (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="0ce93-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="0ce93-329">Atleidimo priežastis (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="0ce93-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="0ce93-330">Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="0ce93-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="0ce93-331">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-331">Human Resources</span></span>                | <span data-ttu-id="0ce93-332">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce93-333">Naujausia samdos data</span><span class="sxs-lookup"><span data-stu-id="0ce93-333">Most recent hire date</span></span> | <span data-ttu-id="0ce93-334">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="0ce93-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0ce93-335">Atleidimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-335">Termination date</span></span>      | <span data-ttu-id="0ce93-336">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0ce93-337">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="0ce93-337">Start date</span></span>            | <span data-ttu-id="0ce93-338">Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="0ce93-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="0ce93-339">Pradinio įdarbinimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-339">Original hire date</span></span>    | <span data-ttu-id="0ce93-340">Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="0ce93-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="0ce93-341">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-341">Compensation</span></span>

<span data-ttu-id="0ce93-342">Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="0ce93-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="0ce93-343">Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="0ce93-344">Įsigaliojimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-344">Effective Date (required)</span></span>
- <span data-ttu-id="0ce93-345">Galiojimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="0ce93-345">Expiration date</span></span>
- <span data-ttu-id="0ce93-346">Užmokesčio tarifas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-346">Pay Rate (required)</span></span>
- <span data-ttu-id="0ce93-347">Užmokesčio tarifo konvertavimas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="0ce93-348">Metinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="0ce93-349">Valandinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="0ce93-350">Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="0ce93-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="0ce93-351">Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="0ce93-352">Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="0ce93-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="0ce93-353">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="0ce93-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="0ce93-354">Socialinio draudimo identifikatorius</span><span class="sxs-lookup"><span data-stu-id="0ce93-354">Social Security identifier</span></span> 

<span data-ttu-id="0ce93-355">Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="0ce93-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="0ce93-356">Šis identifikatorius turi būti **SSN** identifikacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="0ce93-357">„Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.</span><span class="sxs-lookup"><span data-stu-id="0ce93-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="0ce93-358">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-358">Primary (required)</span></span>
- <span data-ttu-id="0ce93-359">Identifikacijos tipas = "SSN"</span><span class="sxs-lookup"><span data-stu-id="0ce93-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="0ce93-360">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-360">Issued Date</span></span>
- <span data-ttu-id="0ce93-361">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-361">Expiration Date</span></span>

<span data-ttu-id="0ce93-362">Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="0ce93-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="0ce93-363">Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.</span><span class="sxs-lookup"><span data-stu-id="0ce93-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="0ce93-364">Banko sąskaitos ir išmokos</span><span class="sxs-lookup"><span data-stu-id="0ce93-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="0ce93-365">Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="0ce93-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="0ce93-366">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-366">Human Resources</span></span>                         | <span data-ttu-id="0ce93-367">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce93-368">Banko sąskaitos numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="0ce93-369">SWIFT kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-369">SWIFT code (required)</span></span>          | <span data-ttu-id="0ce93-370">**Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="0ce93-371">Filialo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="0ce93-372">Banko sąskaitos tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-372">Bank account type (required)</span></span>   | <span data-ttu-id="0ce93-373">**Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="0ce93-374">Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="0ce93-375">Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke.</span><span class="sxs-lookup"><span data-stu-id="0ce93-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="0ce93-376">Visos kitos nelikutinės sąskaitos yra ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="0ce93-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="0ce93-377">Adresas</span><span class="sxs-lookup"><span data-stu-id="0ce93-377">Address information</span></span>

<span data-ttu-id="0ce93-378">Kiekvienas darbuotojas turi turėti vieną pirminę vietą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-378">Every employee must have one primary location.</span></span> <span data-ttu-id="0ce93-379">„Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.</span><span class="sxs-lookup"><span data-stu-id="0ce93-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="0ce93-380">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-380">Primary (required)</span></span>
- <span data-ttu-id="0ce93-381">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-381">Country/region (required)</span></span>
- <span data-ttu-id="0ce93-382">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="0ce93-383">Gatvė (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-383">Street (required)</span></span>
- <span data-ttu-id="0ce93-384">Gatvės numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-384">Street Number (required)</span></span>
- <span data-ttu-id="0ce93-385">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="0ce93-385">Building Complement</span></span>
- <span data-ttu-id="0ce93-386">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-386">City (required)</span></span>
- <span data-ttu-id="0ce93-387">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-387">State (required)</span></span>
- <span data-ttu-id="0ce93-388">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="0ce93-389">Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje</span><span class="sxs-lookup"><span data-stu-id="0ce93-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="0ce93-390">Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="0ce93-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="0ce93-391">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="0ce93-391">Departments are required on positions.</span></span>
- <span data-ttu-id="0ce93-392">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="0ce93-393">Galite sukonfigūruoti „Human Resources“, kad prie pareigų būtų nurodytas padalinys.</span><span class="sxs-lookup"><span data-stu-id="0ce93-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="0ce93-394">Norėdami tai atlikti, eikite į **Bendrinamos personalo pareigos > Pareigos > Prie pareigų reikalauti padalinių**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="0ce93-395">Rekomenduojame integruojant šį parametrą taikyti.</span><span class="sxs-lookup"><span data-stu-id="0ce93-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="0ce93-396">Pareigų rūšys</span><span class="sxs-lookup"><span data-stu-id="0ce93-396">Job types</span></span>

<span data-ttu-id="0ce93-397">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0ce93-398">Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="0ce93-399">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="0ce93-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0ce93-400">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0ce93-401">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-402">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="0ce93-402">Job type</span></span>   | <span data-ttu-id="0ce93-403">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0ce93-404">Valandinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-404">Hourly</span></span>     | <span data-ttu-id="0ce93-405">Valandinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-405">Hourly</span></span>      |
| <span data-ttu-id="0ce93-406">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-406">Salaried</span></span>   | <span data-ttu-id="0ce93-407">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="0ce93-408">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="0ce93-408">Position types</span></span> 

<span data-ttu-id="0ce93-409">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="0ce93-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0ce93-410">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="0ce93-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0ce93-411">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-412">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="0ce93-412">Position type</span></span>   | <span data-ttu-id="0ce93-413">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0ce93-414">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-414">Full-time</span></span>       | <span data-ttu-id="0ce93-415">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-415">Full time employee</span></span> |
| <span data-ttu-id="0ce93-416">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-416">Part-time</span></span>       | <span data-ttu-id="0ce93-417">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0ce93-418">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-418">Reason codes</span></span>

<span data-ttu-id="0ce93-419">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="0ce93-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0ce93-420">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0ce93-421">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-422">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="0ce93-422">Reason code</span></span>    | <span data-ttu-id="0ce93-423">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-423">Description</span></span>      | <span data-ttu-id="0ce93-424">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="0ce93-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="0ce93-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="0ce93-425">RESIGNATION</span></span>    | <span data-ttu-id="0ce93-426">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-426">Resignation</span></span>      | <span data-ttu-id="0ce93-427">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-427">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="0ce93-428">TERMINATION</span></span>    | <span data-ttu-id="0ce93-429">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-429">Termination</span></span>      | <span data-ttu-id="0ce93-430">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-430">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="0ce93-431">RETIREMENT</span></span>     | <span data-ttu-id="0ce93-432">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="0ce93-432">Retirement</span></span>       | <span data-ttu-id="0ce93-433">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-433">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-434">KITA</span><span class="sxs-lookup"><span data-stu-id="0ce93-434">OTHER</span></span>          | <span data-ttu-id="0ce93-435">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="0ce93-435">Other Reasons</span></span>    | <span data-ttu-id="0ce93-436">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-436">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="0ce93-437">DEATH</span></span>          | <span data-ttu-id="0ce93-438">Mirtis</span><span class="sxs-lookup"><span data-stu-id="0ce93-438">Death</span></span>            | <span data-ttu-id="0ce93-439">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-439">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0ce93-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="0ce93-441">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="0ce93-441">Leave of Absence</span></span> | <span data-ttu-id="0ce93-442">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-442">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0ce93-443">CONTRACTEND</span></span>    | <span data-ttu-id="0ce93-444">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="0ce93-444">End of Contract</span></span>  | <span data-ttu-id="0ce93-445">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-445">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0ce93-446">SALARYCHANGE</span></span>   | <span data-ttu-id="0ce93-447">Atlyginimo pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-447">Change of Salary</span></span> | <span data-ttu-id="0ce93-448">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="0ce93-449">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="0ce93-449">Marital status</span></span>

<span data-ttu-id="0ce93-450">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0ce93-451">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0ce93-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-452">Human Resources</span></span>                 | <span data-ttu-id="0ce93-453">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="0ce93-454">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-454">Married</span></span>                | <span data-ttu-id="0ce93-455">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-455">Married</span></span>              |
| <span data-ttu-id="0ce93-456">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-456">Single</span></span>                 | <span data-ttu-id="0ce93-457">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-457">Single</span></span>               |
| <span data-ttu-id="0ce93-458">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="0ce93-458">Widowed</span></span>                | <span data-ttu-id="0ce93-459">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="0ce93-459">Widowed</span></span>              |
| <span data-ttu-id="0ce93-460">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="0ce93-460">Divorced</span></span>               | <span data-ttu-id="0ce93-461">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="0ce93-461">Divorced</span></span>             |
| <span data-ttu-id="0ce93-462">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="0ce93-462">Registered Partnership</span></span> | <span data-ttu-id="0ce93-463">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="0ce93-463">Domestic Partnership</span></span> |
| <span data-ttu-id="0ce93-464">None</span><span class="sxs-lookup"><span data-stu-id="0ce93-464">None</span></span>                   | <span data-ttu-id="0ce93-465">None</span><span class="sxs-lookup"><span data-stu-id="0ce93-465">None</span></span>                 |
| <span data-ttu-id="0ce93-466">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="0ce93-466">Cohabiting</span></span>             | <span data-ttu-id="0ce93-467">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="0ce93-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="0ce93-468">Giminė</span><span class="sxs-lookup"><span data-stu-id="0ce93-468">Gender</span></span>

<span data-ttu-id="0ce93-469">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0ce93-470">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0ce93-471">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-471">Human Resources</span></span>       | <span data-ttu-id="0ce93-472">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="0ce93-473">Vyras</span><span class="sxs-lookup"><span data-stu-id="0ce93-473">Male</span></span>         | <span data-ttu-id="0ce93-474">Vyras</span><span class="sxs-lookup"><span data-stu-id="0ce93-474">Male</span></span>            |
| <span data-ttu-id="0ce93-475">Moteris</span><span class="sxs-lookup"><span data-stu-id="0ce93-475">Female</span></span>       | <span data-ttu-id="0ce93-476">Moteris</span><span class="sxs-lookup"><span data-stu-id="0ce93-476">Female</span></span>          |
| <span data-ttu-id="0ce93-477">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="0ce93-477">Non-specific</span></span> | <span data-ttu-id="0ce93-478">*Nepalaikoma*</span><span class="sxs-lookup"><span data-stu-id="0ce93-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0ce93-479">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-479">Earning codes</span></span>

<span data-ttu-id="0ce93-480">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0ce93-481">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0ce93-482">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0ce93-483">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="0ce93-483">Supported frequencies</span></span>

- <span data-ttu-id="0ce93-484">Visos</span><span class="sxs-lookup"><span data-stu-id="0ce93-484">All</span></span>
- <span data-ttu-id="0ce93-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0ce93-485">EVERYPAY</span></span>
- <span data-ttu-id="0ce93-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0ce93-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0ce93-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0ce93-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0ce93-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0ce93-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0ce93-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-489">1OFMTH</span></span>
- <span data-ttu-id="0ce93-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-490">LASTOFMTH</span></span>
- <span data-ttu-id="0ce93-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-491">2OFMTH</span></span>
- <span data-ttu-id="0ce93-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-492">3OFMTH</span></span>
- <span data-ttu-id="0ce93-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-493">4OFMTH</span></span>
- <span data-ttu-id="0ce93-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-494">5OFMTH</span></span>
- <span data-ttu-id="0ce93-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-495">1N2OFMTH</span></span>
- <span data-ttu-id="0ce93-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-496">3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-497">1N3OFMTH</span></span>
- <span data-ttu-id="0ce93-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-498">1N4OFMTH</span></span>
- <span data-ttu-id="0ce93-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-499">2N3OFMTH</span></span>
- <span data-ttu-id="0ce93-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-500">2N4OFMTH</span></span>
- <span data-ttu-id="0ce93-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="0ce93-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="0ce93-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0ce93-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0ce93-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0ce93-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0ce93-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0ce93-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0ce93-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0ce93-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0ce93-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0ce93-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0ce93-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0ce93-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0ce93-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0ce93-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0ce93-513">Adresai</span><span class="sxs-lookup"><span data-stu-id="0ce93-513">Addresses</span></span>

<span data-ttu-id="0ce93-514">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="0ce93-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0ce93-515">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="0ce93-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0ce93-516">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-516">Human Resources</span></span>          | <span data-ttu-id="0ce93-517">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="0ce93-518">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="0ce93-518">Country/Region</span></span>  | <span data-ttu-id="0ce93-519">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-519">Country Code</span></span>          |
| <span data-ttu-id="0ce93-520">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-520">Zip/Postal Code</span></span> | <span data-ttu-id="0ce93-521">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="0ce93-521">Postal Code</span></span>           |
| <span data-ttu-id="0ce93-522">Apskritis</span><span class="sxs-lookup"><span data-stu-id="0ce93-522">State</span></span>           | <span data-ttu-id="0ce93-523">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-523">State Code</span></span>            |
| <span data-ttu-id="0ce93-524">Miestas</span><span class="sxs-lookup"><span data-stu-id="0ce93-524">City</span></span>            | <span data-ttu-id="0ce93-525">Miestas</span><span class="sxs-lookup"><span data-stu-id="0ce93-525">City</span></span>                  |
| <span data-ttu-id="0ce93-526">Apygarda</span><span class="sxs-lookup"><span data-stu-id="0ce93-526">County</span></span>          | <span data-ttu-id="0ce93-527">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="0ce93-527">County (Municipality)</span></span> |
| <span data-ttu-id="0ce93-528">Gatvė</span><span class="sxs-lookup"><span data-stu-id="0ce93-528">Street</span></span>          | <span data-ttu-id="0ce93-529">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="0ce93-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="0ce93-530">Mokesčių regionai</span><span class="sxs-lookup"><span data-stu-id="0ce93-530">Tax regions</span></span>

<span data-ttu-id="0ce93-531">Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="0ce93-532">Mokesčių regionai yra susieti su „Dayforce“ vietų adresais.</span><span class="sxs-lookup"><span data-stu-id="0ce93-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="0ce93-533">Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis.</span><span class="sxs-lookup"><span data-stu-id="0ce93-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="0ce93-534">Mokesčių regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-534">Tax region (required)</span></span>
- <span data-ttu-id="0ce93-535">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-535">Country/Region (required)</span></span>
- <span data-ttu-id="0ce93-536">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-536">State (required)</span></span>
- <span data-ttu-id="0ce93-537">Apygarda</span><span class="sxs-lookup"><span data-stu-id="0ce93-537">County</span></span> 
- <span data-ttu-id="0ce93-538">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="0ce93-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="0ce93-539">Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje</span><span class="sxs-lookup"><span data-stu-id="0ce93-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="0ce93-540">Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="0ce93-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="0ce93-541">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="0ce93-541">Departments are required on positions.</span></span>
- <span data-ttu-id="0ce93-542">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="0ce93-543">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="0ce93-543">Job types</span></span>

<span data-ttu-id="0ce93-544">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0ce93-545">Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="0ce93-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="0ce93-546">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="0ce93-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0ce93-547">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0ce93-548">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-549">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="0ce93-549">Job type</span></span>   | <span data-ttu-id="0ce93-550">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0ce93-551">Valandinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-551">Hourly</span></span>     | <span data-ttu-id="0ce93-552">MX valandinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-552">MX Hourly</span></span>   |
| <span data-ttu-id="0ce93-553">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-553">Salaried</span></span>   | <span data-ttu-id="0ce93-554">MX fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="0ce93-555">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="0ce93-555">Position types</span></span> 

<span data-ttu-id="0ce93-556">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="0ce93-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0ce93-557">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="0ce93-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0ce93-558">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-559">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="0ce93-559">Position type</span></span>   | <span data-ttu-id="0ce93-560">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0ce93-561">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-561">Full-time</span></span>       | <span data-ttu-id="0ce93-562">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-562">Full time employee</span></span> |
| <span data-ttu-id="0ce93-563">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-563">Part-time</span></span>       | <span data-ttu-id="0ce93-564">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="0ce93-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0ce93-565">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-565">Reason codes</span></span>

<span data-ttu-id="0ce93-566">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="0ce93-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0ce93-567">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="0ce93-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0ce93-568">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-569">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="0ce93-569">Reason code</span></span>            | <span data-ttu-id="0ce93-570">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-570">Description</span></span>                    | <span data-ttu-id="0ce93-571">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="0ce93-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="0ce93-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="0ce93-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="0ce93-573">Išvykimas prieš pirmą algalapį</span><span class="sxs-lookup"><span data-stu-id="0ce93-573">Departure before first payroll</span></span> | <span data-ttu-id="0ce93-574">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-574">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="0ce93-575">RESIGNATION</span></span>            | <span data-ttu-id="0ce93-576">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-576">Resignation</span></span>                    | <span data-ttu-id="0ce93-577">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-577">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="0ce93-578">PENSION</span></span>                | <span data-ttu-id="0ce93-579">Pensija</span><span class="sxs-lookup"><span data-stu-id="0ce93-579">Pension</span></span>                        | <span data-ttu-id="0ce93-580">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-580">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="0ce93-581">TERMINATION</span></span>            | <span data-ttu-id="0ce93-582">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-582">Termination</span></span>                    | <span data-ttu-id="0ce93-583">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-583">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="0ce93-584">RETIREMENT</span></span>             | <span data-ttu-id="0ce93-585">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="0ce93-585">Retirement</span></span>                     | <span data-ttu-id="0ce93-586">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-586">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="0ce93-587">ABSENTEE</span></span>               | <span data-ttu-id="0ce93-588">Nesantysis</span><span class="sxs-lookup"><span data-stu-id="0ce93-588">Absentee</span></span>                       | <span data-ttu-id="0ce93-589">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-589">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-590">KITA</span><span class="sxs-lookup"><span data-stu-id="0ce93-590">OTHER</span></span>                  | <span data-ttu-id="0ce93-591">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="0ce93-591">Other Reasons</span></span>                  | <span data-ttu-id="0ce93-592">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-592">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="0ce93-593">CLOSURE</span></span>                | <span data-ttu-id="0ce93-594">Įmonės uždarymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-594">Business Closure</span></span>               | <span data-ttu-id="0ce93-595">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-595">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="0ce93-596">DEATH</span></span>                  | <span data-ttu-id="0ce93-597">Mirtis</span><span class="sxs-lookup"><span data-stu-id="0ce93-597">Death</span></span>                          | <span data-ttu-id="0ce93-598">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-598">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0ce93-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="0ce93-600">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="0ce93-600">Leave of Absence</span></span>               | <span data-ttu-id="0ce93-601">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-601">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0ce93-602">CONTRACTEND</span></span>            | <span data-ttu-id="0ce93-603">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="0ce93-603">End of Contract</span></span>                | <span data-ttu-id="0ce93-604">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="0ce93-604">Terminate worker</span></span>     |
| <span data-ttu-id="0ce93-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0ce93-605">SALARYCHANGE</span></span>           | <span data-ttu-id="0ce93-606">Atlyginimo keitimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-606">Change of Salary</span></span>               | <span data-ttu-id="0ce93-607">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="0ce93-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="0ce93-608">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="0ce93-608">Terms of employment</span></span>

<span data-ttu-id="0ce93-609">Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="0ce93-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="0ce93-610">Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.</span><span class="sxs-lookup"><span data-stu-id="0ce93-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="0ce93-611">Šios įdarbinimo sąlygos ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="0ce93-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="0ce93-612">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="0ce93-612">Terms of employment</span></span>   | <span data-ttu-id="0ce93-613">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ce93-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="0ce93-614">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="0ce93-614">Regular</span></span>               | <span data-ttu-id="0ce93-615">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="0ce93-615">Regular</span></span>     |
| <span data-ttu-id="0ce93-616">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="0ce93-616">Direct</span></span>                | <span data-ttu-id="0ce93-617">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="0ce93-617">Direct</span></span>      |
| <span data-ttu-id="0ce93-618">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="0ce93-618">Internship</span></span>            | <span data-ttu-id="0ce93-619">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="0ce93-619">Internship</span></span>  |
| <span data-ttu-id="0ce93-620">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-620">Permanent</span></span>             | <span data-ttu-id="0ce93-621">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="0ce93-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="0ce93-622">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="0ce93-622">Marital status</span></span>

<span data-ttu-id="0ce93-623">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0ce93-624">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0ce93-625">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-625">Human Resources</span></span>                 | <span data-ttu-id="0ce93-626">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="0ce93-627">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-627">Married</span></span>                | <span data-ttu-id="0ce93-628">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-628">Married</span></span>                   |
| <span data-ttu-id="0ce93-629">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-629">Single</span></span>                 | <span data-ttu-id="0ce93-630">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="0ce93-630">Single</span></span>                    |
| <span data-ttu-id="0ce93-631">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="0ce93-631">Widowed</span></span>                | <span data-ttu-id="0ce93-632">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="0ce93-632">Widowed</span></span>                   |
| <span data-ttu-id="0ce93-633">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="0ce93-633">Divorced</span></span>               | <span data-ttu-id="0ce93-634">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="0ce93-634">Divorced</span></span>                  |
| <span data-ttu-id="0ce93-635">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="0ce93-635">Registered Partnership</span></span> | <span data-ttu-id="0ce93-636">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="0ce93-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="0ce93-637">None</span><span class="sxs-lookup"><span data-stu-id="0ce93-637">None</span></span>                   | <span data-ttu-id="0ce93-638">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0ce93-639">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="0ce93-639">Cohabiting</span></span>             | <span data-ttu-id="0ce93-640">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="0ce93-641">Giminė</span><span class="sxs-lookup"><span data-stu-id="0ce93-641">Gender</span></span>

<span data-ttu-id="0ce93-642">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0ce93-643">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0ce93-644">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-644">Human Resources</span></span>       | <span data-ttu-id="0ce93-645">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="0ce93-646">Vyras</span><span class="sxs-lookup"><span data-stu-id="0ce93-646">Male</span></span>         | <span data-ttu-id="0ce93-647">Vyras</span><span class="sxs-lookup"><span data-stu-id="0ce93-647">Male</span></span>                      |
| <span data-ttu-id="0ce93-648">Moteris</span><span class="sxs-lookup"><span data-stu-id="0ce93-648">Female</span></span>       | <span data-ttu-id="0ce93-649">Moteris</span><span class="sxs-lookup"><span data-stu-id="0ce93-649">Female</span></span>                    |
| <span data-ttu-id="0ce93-650">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="0ce93-650">Non-specific</span></span> | <span data-ttu-id="0ce93-651">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="0ce93-652">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="0ce93-652">Payment method</span></span>

<span data-ttu-id="0ce93-653">Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="0ce93-654">Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0ce93-655">Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="0ce93-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="0ce93-656">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-656">Human Resources</span></span>             | <span data-ttu-id="0ce93-657">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="0ce93-658">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="0ce93-658">Cash</span></span>               | <span data-ttu-id="0ce93-659">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="0ce93-659">Cash</span></span>                      |
| <span data-ttu-id="0ce93-660">Elektroninis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="0ce93-660">Electronic Payment</span></span> | <span data-ttu-id="0ce93-661">Perkelti</span><span class="sxs-lookup"><span data-stu-id="0ce93-661">Transfer</span></span>                  |
| <span data-ttu-id="0ce93-662">Tikrinti</span><span class="sxs-lookup"><span data-stu-id="0ce93-662">Check</span></span>              | <span data-ttu-id="0ce93-663">Čekis</span><span class="sxs-lookup"><span data-stu-id="0ce93-663">Cheque</span></span>                    |
| <span data-ttu-id="0ce93-664">Banko čekis</span><span class="sxs-lookup"><span data-stu-id="0ce93-664">Bank Draft</span></span>         | <span data-ttu-id="0ce93-665">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0ce93-666">Kiti</span><span class="sxs-lookup"><span data-stu-id="0ce93-666">Other</span></span>              | <span data-ttu-id="0ce93-667">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="0ce93-668">Banko sąskaitos tipas</span><span class="sxs-lookup"><span data-stu-id="0ce93-668">Bank account type</span></span>

<span data-ttu-id="0ce93-669">Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti.</span><span class="sxs-lookup"><span data-stu-id="0ce93-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="0ce93-670">Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="0ce93-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="0ce93-671">Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="0ce93-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="0ce93-672">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-672">Human Resources</span></span>            | <span data-ttu-id="0ce93-673">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="0ce93-674">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-674">Checking Account</span></span>  | <span data-ttu-id="0ce93-675">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-675">CheckingAccount</span></span>           |
| <span data-ttu-id="0ce93-676">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-676">Payroll Account</span></span>   | <span data-ttu-id="0ce93-677">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-677">PayrollAccount</span></span>            |
| <span data-ttu-id="0ce93-678">Taupomoji sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-678">Savings Account</span></span>   | <span data-ttu-id="0ce93-679">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0ce93-680">„BankGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-680">BankGirot account</span></span> | <span data-ttu-id="0ce93-681">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0ce93-682">„PlusGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="0ce93-682">PlusGirot account</span></span> | <span data-ttu-id="0ce93-683">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="0ce93-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0ce93-684">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="0ce93-684">Earning codes</span></span>

<span data-ttu-id="0ce93-685">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0ce93-686">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="0ce93-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0ce93-687">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="0ce93-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0ce93-688">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="0ce93-688">Supported frequencies</span></span>

- <span data-ttu-id="0ce93-689">Visos</span><span class="sxs-lookup"><span data-stu-id="0ce93-689">All</span></span>
- <span data-ttu-id="0ce93-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0ce93-690">EVERYPAY</span></span>
- <span data-ttu-id="0ce93-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0ce93-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0ce93-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0ce93-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0ce93-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0ce93-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0ce93-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-694">1OFMTH</span></span>
- <span data-ttu-id="0ce93-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-695">LASTOFMTH</span></span>
- <span data-ttu-id="0ce93-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-696">2OFMTH</span></span>
- <span data-ttu-id="0ce93-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-697">3OFMTH</span></span>
- <span data-ttu-id="0ce93-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-698">4OFMTH</span></span>
- <span data-ttu-id="0ce93-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-699">5OFMTH</span></span>
- <span data-ttu-id="0ce93-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-700">1N2OFMTH</span></span>
- <span data-ttu-id="0ce93-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-701">3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-702">1N3OFMTH</span></span>
- <span data-ttu-id="0ce93-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-703">1N4OFMTH</span></span>
- <span data-ttu-id="0ce93-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-704">2N3OFMTH</span></span>
- <span data-ttu-id="0ce93-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-705">2N4OFMTH</span></span>
- <span data-ttu-id="0ce93-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="0ce93-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="0ce93-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0ce93-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0ce93-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0ce93-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0ce93-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0ce93-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0ce93-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0ce93-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0ce93-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0ce93-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0ce93-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0ce93-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0ce93-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0ce93-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0ce93-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0ce93-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0ce93-718">Adresai</span><span class="sxs-lookup"><span data-stu-id="0ce93-718">Addresses</span></span>

<span data-ttu-id="0ce93-719">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="0ce93-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0ce93-720">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="0ce93-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0ce93-721">Personalas</span><span class="sxs-lookup"><span data-stu-id="0ce93-721">Human Resources</span></span>              | <span data-ttu-id="0ce93-722">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="0ce93-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="0ce93-723">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="0ce93-723">Country/Region</span></span>      | <span data-ttu-id="0ce93-724">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-724">Country Code</span></span>          |
| <span data-ttu-id="0ce93-725">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-725">Zip/Postal Code</span></span>     | <span data-ttu-id="0ce93-726">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="0ce93-726">Postal Code</span></span>           |
| <span data-ttu-id="0ce93-727">Apskritis</span><span class="sxs-lookup"><span data-stu-id="0ce93-727">State</span></span>               | <span data-ttu-id="0ce93-728">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="0ce93-728">State Code</span></span>            |
| <span data-ttu-id="0ce93-729">Miestas</span><span class="sxs-lookup"><span data-stu-id="0ce93-729">City</span></span>                | <span data-ttu-id="0ce93-730">Miestas</span><span class="sxs-lookup"><span data-stu-id="0ce93-730">City</span></span>                  |
| <span data-ttu-id="0ce93-731">Apygarda</span><span class="sxs-lookup"><span data-stu-id="0ce93-731">County</span></span>              | <span data-ttu-id="0ce93-732">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="0ce93-732">County (Municipality)</span></span> |
| <span data-ttu-id="0ce93-733">Gatvė</span><span class="sxs-lookup"><span data-stu-id="0ce93-733">Street</span></span>              | <span data-ttu-id="0ce93-734">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="0ce93-734">Address Line 1</span></span>        |
| <span data-ttu-id="0ce93-735">Gatvė, namo nr.</span><span class="sxs-lookup"><span data-stu-id="0ce93-735">Street Number</span></span>       | <span data-ttu-id="0ce93-736">2 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="0ce93-736">Address Line 2</span></span>        |
| <span data-ttu-id="0ce93-737">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="0ce93-737">Building Complement</span></span> | <span data-ttu-id="0ce93-738">5 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="0ce93-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="0ce93-739">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="0ce93-739">Passport number</span></span>

<span data-ttu-id="0ce93-740">Darbuotojai gali paskelbti paso informaciją.</span><span class="sxs-lookup"><span data-stu-id="0ce93-740">Employees can declare passport information.</span></span> <span data-ttu-id="0ce93-741">Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.</span><span class="sxs-lookup"><span data-stu-id="0ce93-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="0ce93-742">Identifikacijos tipas = "Pasas"</span><span class="sxs-lookup"><span data-stu-id="0ce93-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="0ce93-743">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-743">Issued Date</span></span>
- <span data-ttu-id="0ce93-744">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="0ce93-744">Expiration Date</span></span>

<span data-ttu-id="0ce93-745">Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="0ce93-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="0ce93-746">Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas.</span><span class="sxs-lookup"><span data-stu-id="0ce93-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="0ce93-747">Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.</span><span class="sxs-lookup"><span data-stu-id="0ce93-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

