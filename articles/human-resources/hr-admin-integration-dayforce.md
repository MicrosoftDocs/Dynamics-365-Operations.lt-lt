---
title: Integravimo su „Dayforce “ konfigūravimas
description: Integravimas tarp „Microsoft Dynamics 365 Human Resources“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šiame straipsnyje. Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Human Resources“, tiek „Dayforce“.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890009"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="92d92-104">Integravimo su „Dayforce “ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="92d92-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="92d92-105">Integravimas tarp „Microsoft Dynamics 365 Human Resources“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šiame straipsnyje.</span><span class="sxs-lookup"><span data-stu-id="92d92-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="92d92-106">Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Human Resources“, tiek „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="92d92-107">Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="92d92-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="92d92-108">Integravimui reikalingi konkretūs duomenys iš „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="92d92-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="92d92-109">Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Human Resources“ taip, kad integravimas būtų palaikomas.</span><span class="sxs-lookup"><span data-stu-id="92d92-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="92d92-110">Integravimui naudojamos šios plačios duomenų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="92d92-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="92d92-111">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="92d92-111">Human resources data</span></span>
- <span data-ttu-id="92d92-112">Atlyginimo dalies duomenys</span><span class="sxs-lookup"><span data-stu-id="92d92-112">Compensation data</span></span>
- <span data-ttu-id="92d92-113">Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="92d92-114">Darbuotojo duomenys</span><span class="sxs-lookup"><span data-stu-id="92d92-114">Worker data</span></span>

<span data-ttu-id="92d92-115">Šiame straipsnyje aprašomi veiksmai, kuriuos reikia vykdyti norint įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="92d92-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="92d92-116">Joje taip pat paaiškinami duomenų tipai ir išsami konfigūravimo informacija, reikalinga integravimui.</span><span class="sxs-lookup"><span data-stu-id="92d92-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="92d92-117">Integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="92d92-117">Enable the integration</span></span>

<span data-ttu-id="92d92-118">Pirmiausia programoje „Human Resources“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="92d92-119">Jei norite, kad sukuriama didžiosios knygos operacija būtų importuota į „Microsoft Dynamics 365 Finance“, taip pat turite sukurti „Microsoft Azure“ saugyklos paskyrą ir įvesti „Azure Storage“ jungimosi eilutę į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="92d92-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="92d92-120">Norėdami įjungti integravimą į „Human Resources“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="92d92-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="92d92-121">Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="92d92-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="92d92-122">Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.</span><span class="sxs-lookup"><span data-stu-id="92d92-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="92d92-123">Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.</span><span class="sxs-lookup"><span data-stu-id="92d92-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="92d92-124">Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="92d92-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="92d92-125">Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas.</span><span class="sxs-lookup"><span data-stu-id="92d92-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="92d92-126">Galite pakeisti šį dažnumą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="92d92-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="92d92-127">Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="92d92-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="92d92-128">Apie „Azure“ saugyklos paskyras</span><span class="sxs-lookup"><span data-stu-id="92d92-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="92d92-129">„Azure Storage“ jungimosi eilučių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="92d92-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="92d92-130">Techninė informacija apie algalapių integravimo įjungimą</span><span class="sxs-lookup"><span data-stu-id="92d92-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="92d92-131">Įjungus algalapių integravimą gaunami du pagrindiniai rezultatai:</span><span class="sxs-lookup"><span data-stu-id="92d92-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="92d92-132">Sukuriamas duomenų eksportavimo projektas pavadinimu Atlyginimų integravimo eksportavimas.</span><span class="sxs-lookup"><span data-stu-id="92d92-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="92d92-133">Šiame projekte yra objektai ir laukai, kurie būtini norint užtikrinti algalapių integravimą.</span><span class="sxs-lookup"><span data-stu-id="92d92-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="92d92-134">Norėdami analizuoti projektą, eikite į **Sistemos administravimas**, pasirinkite plytelę **Duomenų valdymas**, tada projektų sąraše atidarykite duomenų projektą.</span><span class="sxs-lookup"><span data-stu-id="92d92-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="92d92-135">Ši paketinė užduotis vykdo duomenų eksportavimo projektą, užšifruoja gautą duomenų paketą ir perduoda duomenų paketo failą į SFTP galinį punktą, sukonfigūruotą ekrane **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="92d92-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="92d92-136">Duomenų paketas, perduotas į SFTP galinį punktą, užšifruojamas naudojant unikalų pakuotės raktą.</span><span class="sxs-lookup"><span data-stu-id="92d92-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="92d92-137">Raktas laikomas „Azure Key Vault“, kurį gali pasiekti tik „Ceridian“.</span><span class="sxs-lookup"><span data-stu-id="92d92-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="92d92-138">Neįmanoma iššifruoti ir išanalizuoti duomenų paketo turinio.</span><span class="sxs-lookup"><span data-stu-id="92d92-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="92d92-139">Jei reikia analizuoti duomenų paketo turinį, reikės rankiniu būdu eksportuoti duomenų projektą Atlyginimų integravimo eksportavimas, jį atsisiųsti ir tada atsidaryti.</span><span class="sxs-lookup"><span data-stu-id="92d92-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="92d92-140">Eksportuojant rankiniu būdu nebus taikomas šifravimas ir paketas nebus perduodamas.</span><span class="sxs-lookup"><span data-stu-id="92d92-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="92d92-141">Tais atvejais, kai integravimo failai yra siunčiami iš „Dynamics 365 Human Resources” UAT arba Smėlio dėžės aplinkos į „Ceridian Dayforce” testavimo aplinką, galite naudoti šį raktų saugyklos URL: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="92d92-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="92d92-142">Jūsų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="92d92-142">Configure your data</span></span> 

<span data-ttu-id="92d92-143">Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="92d92-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="92d92-144">Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir atlyginimo dalies informaciją.</span><span class="sxs-lookup"><span data-stu-id="92d92-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="92d92-145">Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="92d92-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="92d92-146">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="92d92-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="92d92-147">Išmokos</span><span class="sxs-lookup"><span data-stu-id="92d92-147">Benefits</span></span> 

<span data-ttu-id="92d92-148">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų atlyginimų dalies planus.</span><span class="sxs-lookup"><span data-stu-id="92d92-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="92d92-149">Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="92d92-150">Išmokų planai</span><span class="sxs-lookup"><span data-stu-id="92d92-150">Benefit plans</span></span>

- <span data-ttu-id="92d92-151">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-151">Plan (required)</span></span>
- <span data-ttu-id="92d92-152">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-152">Type (required)</span></span>
- <span data-ttu-id="92d92-153">Poveikis algalapiui (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-153">Payroll impact (required)</span></span>
- <span data-ttu-id="92d92-154">Susigrąžinti skolas</span><span class="sxs-lookup"><span data-stu-id="92d92-154">Recover arrears</span></span>
- <span data-ttu-id="92d92-155">Atskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="92d92-155">Deduction method</span></span>
- <span data-ttu-id="92d92-156">Atskaitymo pirmumas</span><span class="sxs-lookup"><span data-stu-id="92d92-156">Deduction priority</span></span>
- <span data-ttu-id="92d92-157">Apribojimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="92d92-157">Limit period</span></span>
- <span data-ttu-id="92d92-158">Limito suma</span><span class="sxs-lookup"><span data-stu-id="92d92-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="92d92-159">Išmokos</span><span class="sxs-lookup"><span data-stu-id="92d92-159">Benefits</span></span>

- <span data-ttu-id="92d92-160">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-160">Plan (required)</span></span>
- <span data-ttu-id="92d92-161">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-161">Type (required)</span></span>
- <span data-ttu-id="92d92-162">Parinktis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-162">Option (required)</span></span>
- <span data-ttu-id="92d92-163">Išmokos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-163">Benefit ID (required)</span></span>
- <span data-ttu-id="92d92-164">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="92d92-164">Frequency</span></span>
- <span data-ttu-id="92d92-165">Pagrindas</span><span class="sxs-lookup"><span data-stu-id="92d92-165">Basis</span></span>
- <span data-ttu-id="92d92-166">Suma arba tarifas</span><span class="sxs-lookup"><span data-stu-id="92d92-166">Amount or rate</span></span>
- <span data-ttu-id="92d92-167">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="92d92-168">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="92d92-168">Supported frequencies</span></span> 

- <span data-ttu-id="92d92-169">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="92d92-169">Weekly</span></span>
- <span data-ttu-id="92d92-170">Už dvi savaites</span><span class="sxs-lookup"><span data-stu-id="92d92-170">Bi-weekly</span></span>
- <span data-ttu-id="92d92-171">Kas pusę mėnesio</span><span class="sxs-lookup"><span data-stu-id="92d92-171">Semi-monthly</span></span>
- <span data-ttu-id="92d92-172">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="92d92-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="92d92-173">Palaikomos bazės</span><span class="sxs-lookup"><span data-stu-id="92d92-173">Supported bases</span></span> 

- <span data-ttu-id="92d92-174">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="92d92-174">Fixed amount</span></span>
- <span data-ttu-id="92d92-175">Pajamų procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="92d92-175">Percent of earnings</span></span>
- <span data-ttu-id="92d92-176">Produktyvios valandos</span><span class="sxs-lookup"><span data-stu-id="92d92-176">Productive hours</span></span>

<span data-ttu-id="92d92-177">„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.</span><span class="sxs-lookup"><span data-stu-id="92d92-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="92d92-178">Pasirinkimas programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="92d92-178">Selection in Human Resources</span></span>        | <span data-ttu-id="92d92-179">Rezultatas „Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="92d92-180">Jokia</span><span class="sxs-lookup"><span data-stu-id="92d92-180">None</span></span>                       | <span data-ttu-id="92d92-181">Nesukuriama jokio atskaitymo.</span><span class="sxs-lookup"><span data-stu-id="92d92-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="92d92-182">Tik atskaitymas</span><span class="sxs-lookup"><span data-stu-id="92d92-182">Deduction only</span></span>             | <span data-ttu-id="92d92-183">Sukuriamas darbuotojo atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="92d92-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="92d92-184">Tik įnašas</span><span class="sxs-lookup"><span data-stu-id="92d92-184">Contribution only</span></span>          | <span data-ttu-id="92d92-185">Sukuriamas darbdavio atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="92d92-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="92d92-186">Atskaitymas ir įnašas</span><span class="sxs-lookup"><span data-stu-id="92d92-186">Deduction and contribution</span></span> | <span data-ttu-id="92d92-187">Sukuriami darbuotojo ir darbdavio atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="92d92-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="92d92-188">Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="92d92-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="92d92-189">Darbuotojų išmokų programos teikimas</span><span class="sxs-lookup"><span data-stu-id="92d92-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="92d92-190">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="92d92-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="92d92-191">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="92d92-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="92d92-192">Užregistruoti ir pašalinti išmokas darbuotojams</span><span class="sxs-lookup"><span data-stu-id="92d92-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="92d92-193">Atlyginimo dalis</span><span class="sxs-lookup"><span data-stu-id="92d92-193">Compensation</span></span> 

<span data-ttu-id="92d92-194">Atlyginimų dalies valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="92d92-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="92d92-195">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios atlyginimo dalies dalies planus.</span><span class="sxs-lookup"><span data-stu-id="92d92-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="92d92-196">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios atlyginimo dalies dalies planus.</span><span class="sxs-lookup"><span data-stu-id="92d92-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="92d92-197">„Dayforce“ naudojama atlyginimo dalies informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="92d92-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="92d92-198">Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="92d92-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="92d92-199">Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.</span><span class="sxs-lookup"><span data-stu-id="92d92-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="92d92-200">Daugiau informacijos apie atlyginimų dalies planus rasite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="92d92-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="92d92-201">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="92d92-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="92d92-202">Kintamosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="92d92-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="92d92-203">Kurti atlyginimų / kompensavimo struktūrą ir planus</span><span class="sxs-lookup"><span data-stu-id="92d92-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="92d92-204">Kompensavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="92d92-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="92d92-205">Kompensavimo proceso nustatymas ir rezultatų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="92d92-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="92d92-206">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="92d92-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="92d92-207">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="92d92-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="92d92-208">Darbai</span><span class="sxs-lookup"><span data-stu-id="92d92-208">Jobs</span></span> 

<span data-ttu-id="92d92-209">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="92d92-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="92d92-210">Daugiau informacijos ieškokite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="92d92-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="92d92-211">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="92d92-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="92d92-212">Naujų darbo vietų nustatymas</span><span class="sxs-lookup"><span data-stu-id="92d92-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="92d92-213">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="92d92-213">Positions</span></span>

<span data-ttu-id="92d92-214">Pareigos yra atskiros užduoties egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="92d92-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="92d92-215">Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="92d92-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="92d92-216">Pareigos egzistuoja padalinyje.</span><span class="sxs-lookup"><span data-stu-id="92d92-216">A position exists in a department.</span></span> <span data-ttu-id="92d92-217">Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="92d92-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="92d92-218">Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:</span><span class="sxs-lookup"><span data-stu-id="92d92-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="92d92-219">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-219">Position (required)</span></span>
- <span data-ttu-id="92d92-220">Aprašas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-220">Description (required)</span></span>
- <span data-ttu-id="92d92-221">Užduotis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-221">Job (required)</span></span>
- <span data-ttu-id="92d92-222">Padalinys (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-222">Department (required)</span></span>
- <span data-ttu-id="92d92-223">Pareigų tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-223">Position type (required)</span></span>
- <span data-ttu-id="92d92-224">Viso etato ekvivalentas</span><span class="sxs-lookup"><span data-stu-id="92d92-224">Full-time equivalent</span></span>
- <span data-ttu-id="92d92-225">Įprastos darbo valandos per metus (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="92d92-226">Apmokama juridinio subjekto (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="92d92-227">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-227">Pay cycle (required)</span></span>
- <span data-ttu-id="92d92-228">Numatytosios finansinės dimensijos – išlaidų centras (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="92d92-229">Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="92d92-230">Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.</span><span class="sxs-lookup"><span data-stu-id="92d92-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="92d92-231">Daugiau informacijos ieškokite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="92d92-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="92d92-232">Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas</span><span class="sxs-lookup"><span data-stu-id="92d92-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="92d92-233">Pareigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="92d92-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="92d92-234">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="92d92-234">Departments</span></span>

<span data-ttu-id="92d92-235">Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį.</span><span class="sxs-lookup"><span data-stu-id="92d92-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="92d92-236">Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą.</span><span class="sxs-lookup"><span data-stu-id="92d92-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="92d92-237">Padalinius galite naudoti norėdami pranešti apie funkcines sritis.</span><span class="sxs-lookup"><span data-stu-id="92d92-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="92d92-238">Padaliniai gali turėti pelno ir nuostolio atsakomybę.</span><span class="sxs-lookup"><span data-stu-id="92d92-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="92d92-239">Daugiau informacijos ieškokite šiuose straipsniuose:</span><span class="sxs-lookup"><span data-stu-id="92d92-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="92d92-240">Padalinio sukūrimas ir susiejimas su padalinių hierarchija</span><span class="sxs-lookup"><span data-stu-id="92d92-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="92d92-241">Apibrėžti naujus padalinius</span><span class="sxs-lookup"><span data-stu-id="92d92-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="92d92-242">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="92d92-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="92d92-243">Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams.</span><span class="sxs-lookup"><span data-stu-id="92d92-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="92d92-244">Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="92d92-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="92d92-245">Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="92d92-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="92d92-246">Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.</span><span class="sxs-lookup"><span data-stu-id="92d92-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="92d92-247">Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="92d92-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="92d92-248">Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="92d92-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="92d92-249">Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.</span><span class="sxs-lookup"><span data-stu-id="92d92-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="92d92-250">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="92d92-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="92d92-251">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-251">Pay cycle (required)</span></span>
- <span data-ttu-id="92d92-252">Mokėjimo ciklo dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="92d92-253">Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="92d92-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="92d92-254">Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="92d92-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="92d92-255">Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui.</span><span class="sxs-lookup"><span data-stu-id="92d92-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="92d92-256">Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="92d92-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="92d92-257">„Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="92d92-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="92d92-258">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-258">Earning codes</span></span>

<span data-ttu-id="92d92-259">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="92d92-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="92d92-260">Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="92d92-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="92d92-261">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="92d92-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="92d92-262">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-262">Earning Code (required)</span></span>
- <span data-ttu-id="92d92-263">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-263">Description</span></span>
- <span data-ttu-id="92d92-264">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="92d92-264">Unit of measure</span></span>
- <span data-ttu-id="92d92-265">Produktyvus</span><span class="sxs-lookup"><span data-stu-id="92d92-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="92d92-266">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="92d92-266">Worker data</span></span>

<span data-ttu-id="92d92-267">Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms.</span><span class="sxs-lookup"><span data-stu-id="92d92-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="92d92-268">Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.</span><span class="sxs-lookup"><span data-stu-id="92d92-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="92d92-269">Galite tvarkyti šią darbininkų informaciją:</span><span class="sxs-lookup"><span data-stu-id="92d92-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="92d92-270">**Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.</span><span class="sxs-lookup"><span data-stu-id="92d92-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="92d92-271">**Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="92d92-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="92d92-272">**Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="92d92-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="92d92-273">**Atlyginimo dalis ir algalapis** – tvarkykite informaciją apie darbininko atlyginimo dalies planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.</span><span class="sxs-lookup"><span data-stu-id="92d92-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="92d92-274">Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="92d92-275">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="92d92-275">General information</span></span>

- <span data-ttu-id="92d92-276">Darbuotojo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-276">Personnel number (required)</span></span>
- <span data-ttu-id="92d92-277">Vardas (būtinas)</span><span class="sxs-lookup"><span data-stu-id="92d92-277">First name (required)</span></span>
- <span data-ttu-id="92d92-278">Pavardė (būtinai)</span><span class="sxs-lookup"><span data-stu-id="92d92-278">Last name (required)</span></span>
- <span data-ttu-id="92d92-279">Antras vardas</span><span class="sxs-lookup"><span data-stu-id="92d92-279">Middle name</span></span>
- <span data-ttu-id="92d92-280">Paaukštinimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-280">Seniority date</span></span>
- <span data-ttu-id="92d92-281">Žinoma kaip</span><span class="sxs-lookup"><span data-stu-id="92d92-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="92d92-282">Asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="92d92-282">Personal information</span></span>

- <span data-ttu-id="92d92-283">Šeiminė padėtis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-283">Marital status (required)</span></span>
- <span data-ttu-id="92d92-284">Gimimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-284">Birth date (required)</span></span>
- <span data-ttu-id="92d92-285">Lytis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-285">Gender (required)</span></span>
- <span data-ttu-id="92d92-286">Asmuo su negalia</span><span class="sxs-lookup"><span data-stu-id="92d92-286">Person with disabilities</span></span>
- <span data-ttu-id="92d92-287">Pilietybės šalies regionas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="92d92-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="92d92-288">Adresas</span><span class="sxs-lookup"><span data-stu-id="92d92-288">Address information</span></span>

- <span data-ttu-id="92d92-289">Pagrindinis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-289">Primary (required)</span></span>
- <span data-ttu-id="92d92-290">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-290">Country/region (required)</span></span>
- <span data-ttu-id="92d92-291">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-291">Postal code (required)</span></span>
- <span data-ttu-id="92d92-292">Gatvės numeris (būtina) (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="92d92-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="92d92-293">Pastatų kompleksas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="92d92-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="92d92-294">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-294">City (required)</span></span>
- <span data-ttu-id="92d92-295">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-295">State (required)</span></span>
- <span data-ttu-id="92d92-296">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="92d92-297">Kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="92d92-297">Contact information</span></span> 

- <span data-ttu-id="92d92-298">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-298">Primary (required)</span></span>
- <span data-ttu-id="92d92-299">Kontakto numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-299">Contact number (required)</span></span>
- <span data-ttu-id="92d92-300">Išplėtimas</span><span class="sxs-lookup"><span data-stu-id="92d92-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="92d92-301">Algalapio informacija ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-301">Payroll information and earning codes</span></span>

<span data-ttu-id="92d92-302">Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="92d92-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="92d92-303">Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.</span><span class="sxs-lookup"><span data-stu-id="92d92-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="92d92-304">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-304">Earning codes</span></span>

- <span data-ttu-id="92d92-305">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-305">Position (required)</span></span>
- <span data-ttu-id="92d92-306">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-306">Earning Code (required)</span></span>
- <span data-ttu-id="92d92-307">Dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-307">Frequency (required)</span></span>
- <span data-ttu-id="92d92-308">Suma (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="92d92-309">Algalapių informacija</span><span class="sxs-lookup"><span data-stu-id="92d92-309">Payroll information</span></span>

- <span data-ttu-id="92d92-310">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="92d92-310">Payment Method</span></span>
- <span data-ttu-id="92d92-311">Ekonominė sritis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-311">Economic Region (required)</span></span>
- <span data-ttu-id="92d92-312">Darbuotojų išmokų ID</span><span class="sxs-lookup"><span data-stu-id="92d92-312">Employee Benefits ID</span></span>
- <span data-ttu-id="92d92-313">Asmens kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-313">National ID Number (required)</span></span>
- <span data-ttu-id="92d92-314">Karo tarnybos numeris</span><span class="sxs-lookup"><span data-stu-id="92d92-314">Military Service Number</span></span>
- <span data-ttu-id="92d92-315">Pamainos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-315">Shift ID (required)</span></span>
- <span data-ttu-id="92d92-316">Mokesčių numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-316">Tax Number (required)</span></span>
- <span data-ttu-id="92d92-317">Sąjungos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-317">Union ID (required)</span></span>
- <span data-ttu-id="92d92-318">Darbo dienos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-318">Work Day ID (required)</span></span>
- <span data-ttu-id="92d92-319">Darbo leidimo numeris</span><span class="sxs-lookup"><span data-stu-id="92d92-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="92d92-320">Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="92d92-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="92d92-321">Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.</span><span class="sxs-lookup"><span data-stu-id="92d92-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="92d92-322">Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="92d92-322">Employment details</span></span>

<span data-ttu-id="92d92-323">Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos.</span><span class="sxs-lookup"><span data-stu-id="92d92-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="92d92-324">„Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="92d92-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="92d92-325">Įdarbinimo pradžios data (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-325">Employment start date (required)</span></span>
- <span data-ttu-id="92d92-326">Įdarbinimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="92d92-326">Employment end date</span></span>
- <span data-ttu-id="92d92-327">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="92d92-327">Start date</span></span>
- <span data-ttu-id="92d92-328">Patikslinta darbo pradžios data</span><span class="sxs-lookup"><span data-stu-id="92d92-328">Adjusted start date</span></span>
- <span data-ttu-id="92d92-329">Atleidimo data (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="92d92-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="92d92-330">Atleidimo priežastis (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="92d92-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="92d92-331">Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="92d92-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="92d92-332">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-332">Human Resources</span></span>                | <span data-ttu-id="92d92-333">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d92-334">Naujausia samdos data</span><span class="sxs-lookup"><span data-stu-id="92d92-334">Most recent hire date</span></span> | <span data-ttu-id="92d92-335">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="92d92-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="92d92-336">Atleidimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-336">Termination date</span></span>      | <span data-ttu-id="92d92-337">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="92d92-338">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="92d92-338">Start date</span></span>            | <span data-ttu-id="92d92-339">Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="92d92-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="92d92-340">Pradinio įdarbinimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-340">Original hire date</span></span>    | <span data-ttu-id="92d92-341">Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="92d92-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="92d92-342">Atlyginimo dalis</span><span class="sxs-lookup"><span data-stu-id="92d92-342">Compensation</span></span>

<span data-ttu-id="92d92-343">Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="92d92-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="92d92-344">Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="92d92-345">Įsigaliojimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-345">Effective Date (required)</span></span>
- <span data-ttu-id="92d92-346">Galiojimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="92d92-346">Expiration date</span></span>
- <span data-ttu-id="92d92-347">Užmokesčio tarifas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-347">Pay Rate (required)</span></span>
- <span data-ttu-id="92d92-348">Užmokesčio tarifo konvertavimas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="92d92-349">Metinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="92d92-350">Valandinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="92d92-351">Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="92d92-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="92d92-352">Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="92d92-353">Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="92d92-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="92d92-354">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="92d92-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="92d92-355">Socialinio draudimo identifikatorius</span><span class="sxs-lookup"><span data-stu-id="92d92-355">Social Security identifier</span></span> 

<span data-ttu-id="92d92-356">Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="92d92-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="92d92-357">Šis identifikatorius turi būti **SSN** identifikacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="92d92-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="92d92-358">„Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.</span><span class="sxs-lookup"><span data-stu-id="92d92-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="92d92-359">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-359">Primary (required)</span></span>
- <span data-ttu-id="92d92-360">Identifikacijos tipas = "SSN"</span><span class="sxs-lookup"><span data-stu-id="92d92-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="92d92-361">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-361">Issued Date</span></span>
- <span data-ttu-id="92d92-362">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-362">Expiration Date</span></span>

<span data-ttu-id="92d92-363">Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="92d92-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="92d92-364">Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.</span><span class="sxs-lookup"><span data-stu-id="92d92-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="92d92-365">Banko sąskaitos ir išmokos</span><span class="sxs-lookup"><span data-stu-id="92d92-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="92d92-366">Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="92d92-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="92d92-367">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-367">Human Resources</span></span>                         | <span data-ttu-id="92d92-368">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d92-369">Banko sąskaitos numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="92d92-370">SWIFT kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-370">SWIFT code (required)</span></span>          | <span data-ttu-id="92d92-371">**Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="92d92-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="92d92-372">Filialo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="92d92-373">Banko sąskaitos tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-373">Bank account type (required)</span></span>   | <span data-ttu-id="92d92-374">**Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="92d92-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="92d92-375">Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**.</span><span class="sxs-lookup"><span data-stu-id="92d92-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="92d92-376">Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke.</span><span class="sxs-lookup"><span data-stu-id="92d92-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="92d92-377">Visos kitos nelikutinės sąskaitos yra ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="92d92-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="92d92-378">Adresas</span><span class="sxs-lookup"><span data-stu-id="92d92-378">Address information</span></span>

<span data-ttu-id="92d92-379">Kiekvienas darbuotojas turi turėti vieną pirminę vietą.</span><span class="sxs-lookup"><span data-stu-id="92d92-379">Every employee must have one primary location.</span></span> <span data-ttu-id="92d92-380">„Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.</span><span class="sxs-lookup"><span data-stu-id="92d92-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="92d92-381">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-381">Primary (required)</span></span>
- <span data-ttu-id="92d92-382">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-382">Country/region (required)</span></span>
- <span data-ttu-id="92d92-383">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="92d92-384">Gatvė (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-384">Street (required)</span></span>
- <span data-ttu-id="92d92-385">Gatvės numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-385">Street Number (required)</span></span>
- <span data-ttu-id="92d92-386">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="92d92-386">Building Complement</span></span>
- <span data-ttu-id="92d92-387">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-387">City (required)</span></span>
- <span data-ttu-id="92d92-388">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-388">State (required)</span></span>
- <span data-ttu-id="92d92-389">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="92d92-390">Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje</span><span class="sxs-lookup"><span data-stu-id="92d92-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="92d92-391">Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="92d92-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="92d92-392">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="92d92-392">Departments are required on positions.</span></span>
- <span data-ttu-id="92d92-393">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="92d92-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="92d92-394">Galite sukonfigūruoti „Human Resources“, kad prie pareigų būtų nurodytas padalinys.</span><span class="sxs-lookup"><span data-stu-id="92d92-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="92d92-395">Norėdami tai atlikti, eikite į **Bendrinamos personalo pareigos > Pareigos > Prie pareigų reikalauti padalinių**.</span><span class="sxs-lookup"><span data-stu-id="92d92-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="92d92-396">Rekomenduojame integruojant šį parametrą taikyti.</span><span class="sxs-lookup"><span data-stu-id="92d92-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="92d92-397">Pareigų rūšys</span><span class="sxs-lookup"><span data-stu-id="92d92-397">Job types</span></span>

<span data-ttu-id="92d92-398">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="92d92-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="92d92-399">Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje.</span><span class="sxs-lookup"><span data-stu-id="92d92-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="92d92-400">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="92d92-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="92d92-401">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="92d92-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="92d92-402">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="92d92-403">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="92d92-403">Job type</span></span>   | <span data-ttu-id="92d92-404">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="92d92-405">Valandinis</span><span class="sxs-lookup"><span data-stu-id="92d92-405">Hourly</span></span>     | <span data-ttu-id="92d92-406">Valandinis</span><span class="sxs-lookup"><span data-stu-id="92d92-406">Hourly</span></span>      |
| <span data-ttu-id="92d92-407">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="92d92-407">Salaried</span></span>   | <span data-ttu-id="92d92-408">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="92d92-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="92d92-409">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="92d92-409">Position types</span></span> 

<span data-ttu-id="92d92-410">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="92d92-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="92d92-411">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="92d92-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="92d92-412">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="92d92-413">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="92d92-413">Position type</span></span>   | <span data-ttu-id="92d92-414">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="92d92-415">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-415">Full-time</span></span>       | <span data-ttu-id="92d92-416">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-416">Full time employee</span></span> |
| <span data-ttu-id="92d92-417">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-417">Part-time</span></span>       | <span data-ttu-id="92d92-418">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="92d92-419">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-419">Reason codes</span></span>

<span data-ttu-id="92d92-420">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="92d92-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="92d92-421">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="92d92-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="92d92-422">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="92d92-423">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="92d92-423">Reason code</span></span>    | <span data-ttu-id="92d92-424">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-424">Description</span></span>      | <span data-ttu-id="92d92-425">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="92d92-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="92d92-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="92d92-426">RESIGNATION</span></span>    | <span data-ttu-id="92d92-427">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="92d92-427">Resignation</span></span>      | <span data-ttu-id="92d92-428">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-428">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="92d92-429">TERMINATION</span></span>    | <span data-ttu-id="92d92-430">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="92d92-430">Termination</span></span>      | <span data-ttu-id="92d92-431">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-431">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="92d92-432">RETIREMENT</span></span>     | <span data-ttu-id="92d92-433">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="92d92-433">Retirement</span></span>       | <span data-ttu-id="92d92-434">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-434">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-435">KITA</span><span class="sxs-lookup"><span data-stu-id="92d92-435">OTHER</span></span>          | <span data-ttu-id="92d92-436">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="92d92-436">Other Reasons</span></span>    | <span data-ttu-id="92d92-437">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-437">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="92d92-438">DEATH</span></span>          | <span data-ttu-id="92d92-439">Mirtis</span><span class="sxs-lookup"><span data-stu-id="92d92-439">Death</span></span>            | <span data-ttu-id="92d92-440">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-440">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="92d92-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="92d92-442">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="92d92-442">Leave of Absence</span></span> | <span data-ttu-id="92d92-443">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-443">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="92d92-444">CONTRACTEND</span></span>    | <span data-ttu-id="92d92-445">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="92d92-445">End of Contract</span></span>  | <span data-ttu-id="92d92-446">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-446">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="92d92-447">SALARYCHANGE</span></span>   | <span data-ttu-id="92d92-448">Atlyginimo pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="92d92-448">Change of Salary</span></span> | <span data-ttu-id="92d92-449">Atlyginimo dalis</span><span class="sxs-lookup"><span data-stu-id="92d92-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="92d92-450">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="92d92-450">Marital status</span></span>

<span data-ttu-id="92d92-451">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="92d92-452">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="92d92-453">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-453">Human Resources</span></span>                 | <span data-ttu-id="92d92-454">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="92d92-455">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-455">Married</span></span>                | <span data-ttu-id="92d92-456">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-456">Married</span></span>              |
| <span data-ttu-id="92d92-457">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-457">Single</span></span>                 | <span data-ttu-id="92d92-458">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-458">Single</span></span>               |
| <span data-ttu-id="92d92-459">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="92d92-459">Widowed</span></span>                | <span data-ttu-id="92d92-460">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="92d92-460">Widowed</span></span>              |
| <span data-ttu-id="92d92-461">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="92d92-461">Divorced</span></span>               | <span data-ttu-id="92d92-462">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="92d92-462">Divorced</span></span>             |
| <span data-ttu-id="92d92-463">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="92d92-463">Registered Partnership</span></span> | <span data-ttu-id="92d92-464">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="92d92-464">Domestic Partnership</span></span> |
| <span data-ttu-id="92d92-465">Nėra</span><span class="sxs-lookup"><span data-stu-id="92d92-465">None</span></span>                   | <span data-ttu-id="92d92-466">Nėra</span><span class="sxs-lookup"><span data-stu-id="92d92-466">None</span></span>                 |
| <span data-ttu-id="92d92-467">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="92d92-467">Cohabiting</span></span>             | <span data-ttu-id="92d92-468">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="92d92-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="92d92-469">Giminė</span><span class="sxs-lookup"><span data-stu-id="92d92-469">Gender</span></span>

<span data-ttu-id="92d92-470">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="92d92-471">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="92d92-472">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-472">Human Resources</span></span>       | <span data-ttu-id="92d92-473">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="92d92-474">Vyras</span><span class="sxs-lookup"><span data-stu-id="92d92-474">Male</span></span>         | <span data-ttu-id="92d92-475">Vyras</span><span class="sxs-lookup"><span data-stu-id="92d92-475">Male</span></span>            |
| <span data-ttu-id="92d92-476">Moteris</span><span class="sxs-lookup"><span data-stu-id="92d92-476">Female</span></span>       | <span data-ttu-id="92d92-477">Moteris</span><span class="sxs-lookup"><span data-stu-id="92d92-477">Female</span></span>          |
| <span data-ttu-id="92d92-478">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="92d92-478">Non-specific</span></span> | <span data-ttu-id="92d92-479">*Nepalaikoma*</span><span class="sxs-lookup"><span data-stu-id="92d92-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="92d92-480">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-480">Earning codes</span></span>

<span data-ttu-id="92d92-481">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="92d92-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="92d92-482">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="92d92-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="92d92-483">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="92d92-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="92d92-484">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="92d92-484">Supported frequencies</span></span>

- <span data-ttu-id="92d92-485">Visos</span><span class="sxs-lookup"><span data-stu-id="92d92-485">All</span></span>
- <span data-ttu-id="92d92-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="92d92-486">EVERYPAY</span></span>
- <span data-ttu-id="92d92-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="92d92-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="92d92-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="92d92-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="92d92-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="92d92-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="92d92-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-490">1OFMTH</span></span>
- <span data-ttu-id="92d92-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-491">LASTOFMTH</span></span>
- <span data-ttu-id="92d92-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-492">2OFMTH</span></span>
- <span data-ttu-id="92d92-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-493">3OFMTH</span></span>
- <span data-ttu-id="92d92-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-494">4OFMTH</span></span>
- <span data-ttu-id="92d92-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-495">5OFMTH</span></span>
- <span data-ttu-id="92d92-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-496">1N2OFMTH</span></span>
- <span data-ttu-id="92d92-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-497">3N4OFMTH</span></span>
- <span data-ttu-id="92d92-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-498">1N3OFMTH</span></span>
- <span data-ttu-id="92d92-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-499">1N4OFMTH</span></span>
- <span data-ttu-id="92d92-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-500">2N3OFMTH</span></span>
- <span data-ttu-id="92d92-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-501">2N4OFMTH</span></span>
- <span data-ttu-id="92d92-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="92d92-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="92d92-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="92d92-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="92d92-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="92d92-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="92d92-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="92d92-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="92d92-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="92d92-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="92d92-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="92d92-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="92d92-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="92d92-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="92d92-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="92d92-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="92d92-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="92d92-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="92d92-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="92d92-514">Adresai</span><span class="sxs-lookup"><span data-stu-id="92d92-514">Addresses</span></span>

<span data-ttu-id="92d92-515">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="92d92-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="92d92-516">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="92d92-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="92d92-517">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-517">Human Resources</span></span>          | <span data-ttu-id="92d92-518">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="92d92-519">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="92d92-519">Country/Region</span></span>  | <span data-ttu-id="92d92-520">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-520">Country Code</span></span>          |
| <span data-ttu-id="92d92-521">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-521">Zip/Postal Code</span></span> | <span data-ttu-id="92d92-522">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="92d92-522">Postal Code</span></span>           |
| <span data-ttu-id="92d92-523">Apskritis</span><span class="sxs-lookup"><span data-stu-id="92d92-523">State</span></span>           | <span data-ttu-id="92d92-524">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-524">State Code</span></span>            |
| <span data-ttu-id="92d92-525">Miestas</span><span class="sxs-lookup"><span data-stu-id="92d92-525">City</span></span>            | <span data-ttu-id="92d92-526">Miestas</span><span class="sxs-lookup"><span data-stu-id="92d92-526">City</span></span>                  |
| <span data-ttu-id="92d92-527">Apygarda</span><span class="sxs-lookup"><span data-stu-id="92d92-527">County</span></span>          | <span data-ttu-id="92d92-528">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="92d92-528">County (Municipality)</span></span> |
| <span data-ttu-id="92d92-529">Gatvė</span><span class="sxs-lookup"><span data-stu-id="92d92-529">Street</span></span>          | <span data-ttu-id="92d92-530">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="92d92-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="92d92-531">Mokesčių regionai</span><span class="sxs-lookup"><span data-stu-id="92d92-531">Tax regions</span></span>

<span data-ttu-id="92d92-532">Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį.</span><span class="sxs-lookup"><span data-stu-id="92d92-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="92d92-533">Mokesčių regionai yra susieti su „Dayforce“ vietų adresais.</span><span class="sxs-lookup"><span data-stu-id="92d92-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="92d92-534">Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis.</span><span class="sxs-lookup"><span data-stu-id="92d92-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="92d92-535">Mokesčių regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-535">Tax region (required)</span></span>
- <span data-ttu-id="92d92-536">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-536">Country/Region (required)</span></span>
- <span data-ttu-id="92d92-537">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-537">State (required)</span></span>
- <span data-ttu-id="92d92-538">Apygarda</span><span class="sxs-lookup"><span data-stu-id="92d92-538">County</span></span> 
- <span data-ttu-id="92d92-539">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="92d92-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="92d92-540">Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje</span><span class="sxs-lookup"><span data-stu-id="92d92-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="92d92-541">Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="92d92-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="92d92-542">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="92d92-542">Departments are required on positions.</span></span>
- <span data-ttu-id="92d92-543">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="92d92-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="92d92-544">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="92d92-544">Job types</span></span>

<span data-ttu-id="92d92-545">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="92d92-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="92d92-546">Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="92d92-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="92d92-547">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="92d92-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="92d92-548">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="92d92-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="92d92-549">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="92d92-550">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="92d92-550">Job type</span></span>   | <span data-ttu-id="92d92-551">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="92d92-552">Valandinis</span><span class="sxs-lookup"><span data-stu-id="92d92-552">Hourly</span></span>     | <span data-ttu-id="92d92-553">MX valandinis</span><span class="sxs-lookup"><span data-stu-id="92d92-553">MX Hourly</span></span>   |
| <span data-ttu-id="92d92-554">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="92d92-554">Salaried</span></span>   | <span data-ttu-id="92d92-555">MX fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="92d92-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="92d92-556">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="92d92-556">Position types</span></span> 

<span data-ttu-id="92d92-557">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="92d92-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="92d92-558">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="92d92-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="92d92-559">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="92d92-560">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="92d92-560">Position type</span></span>   | <span data-ttu-id="92d92-561">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="92d92-562">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-562">Full-time</span></span>       | <span data-ttu-id="92d92-563">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-563">Full time employee</span></span> |
| <span data-ttu-id="92d92-564">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-564">Part-time</span></span>       | <span data-ttu-id="92d92-565">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="92d92-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="92d92-566">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-566">Reason codes</span></span>

<span data-ttu-id="92d92-567">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="92d92-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="92d92-568">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="92d92-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="92d92-569">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="92d92-570">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="92d92-570">Reason code</span></span>            | <span data-ttu-id="92d92-571">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-571">Description</span></span>                    | <span data-ttu-id="92d92-572">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="92d92-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="92d92-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="92d92-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="92d92-574">Išvykimas prieš pirmą algalapį</span><span class="sxs-lookup"><span data-stu-id="92d92-574">Departure before first payroll</span></span> | <span data-ttu-id="92d92-575">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-575">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="92d92-576">RESIGNATION</span></span>            | <span data-ttu-id="92d92-577">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="92d92-577">Resignation</span></span>                    | <span data-ttu-id="92d92-578">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-578">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="92d92-579">PENSION</span></span>                | <span data-ttu-id="92d92-580">Pensija</span><span class="sxs-lookup"><span data-stu-id="92d92-580">Pension</span></span>                        | <span data-ttu-id="92d92-581">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-581">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="92d92-582">TERMINATION</span></span>            | <span data-ttu-id="92d92-583">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="92d92-583">Termination</span></span>                    | <span data-ttu-id="92d92-584">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-584">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="92d92-585">RETIREMENT</span></span>             | <span data-ttu-id="92d92-586">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="92d92-586">Retirement</span></span>                     | <span data-ttu-id="92d92-587">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-587">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="92d92-588">ABSENTEE</span></span>               | <span data-ttu-id="92d92-589">Nesantysis</span><span class="sxs-lookup"><span data-stu-id="92d92-589">Absentee</span></span>                       | <span data-ttu-id="92d92-590">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-590">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-591">KITA</span><span class="sxs-lookup"><span data-stu-id="92d92-591">OTHER</span></span>                  | <span data-ttu-id="92d92-592">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="92d92-592">Other Reasons</span></span>                  | <span data-ttu-id="92d92-593">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-593">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="92d92-594">CLOSURE</span></span>                | <span data-ttu-id="92d92-595">Įmonės uždarymas</span><span class="sxs-lookup"><span data-stu-id="92d92-595">Business Closure</span></span>               | <span data-ttu-id="92d92-596">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-596">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="92d92-597">DEATH</span></span>                  | <span data-ttu-id="92d92-598">Mirtis</span><span class="sxs-lookup"><span data-stu-id="92d92-598">Death</span></span>                          | <span data-ttu-id="92d92-599">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-599">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="92d92-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="92d92-601">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="92d92-601">Leave of Absence</span></span>               | <span data-ttu-id="92d92-602">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-602">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="92d92-603">CONTRACTEND</span></span>            | <span data-ttu-id="92d92-604">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="92d92-604">End of Contract</span></span>                | <span data-ttu-id="92d92-605">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="92d92-605">Terminate worker</span></span>     |
| <span data-ttu-id="92d92-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="92d92-606">SALARYCHANGE</span></span>           | <span data-ttu-id="92d92-607">Atlyginimo keitimas</span><span class="sxs-lookup"><span data-stu-id="92d92-607">Change of Salary</span></span>               | <span data-ttu-id="92d92-608">Atlyginimo dalis</span><span class="sxs-lookup"><span data-stu-id="92d92-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="92d92-609">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="92d92-609">Terms of employment</span></span>

<span data-ttu-id="92d92-610">Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="92d92-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="92d92-611">Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.</span><span class="sxs-lookup"><span data-stu-id="92d92-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="92d92-612">Šios įdarbinimo sąlygos ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="92d92-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="92d92-613">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="92d92-613">Terms of employment</span></span>   | <span data-ttu-id="92d92-614">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92d92-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="92d92-615">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="92d92-615">Regular</span></span>               | <span data-ttu-id="92d92-616">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="92d92-616">Regular</span></span>     |
| <span data-ttu-id="92d92-617">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="92d92-617">Direct</span></span>                | <span data-ttu-id="92d92-618">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="92d92-618">Direct</span></span>      |
| <span data-ttu-id="92d92-619">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="92d92-619">Internship</span></span>            | <span data-ttu-id="92d92-620">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="92d92-620">Internship</span></span>  |
| <span data-ttu-id="92d92-621">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="92d92-621">Permanent</span></span>             | <span data-ttu-id="92d92-622">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="92d92-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="92d92-623">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="92d92-623">Marital status</span></span>

<span data-ttu-id="92d92-624">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="92d92-625">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="92d92-626">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-626">Human Resources</span></span>                 | <span data-ttu-id="92d92-627">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="92d92-628">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-628">Married</span></span>                | <span data-ttu-id="92d92-629">Vedęs/ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-629">Married</span></span>                   |
| <span data-ttu-id="92d92-630">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-630">Single</span></span>                 | <span data-ttu-id="92d92-631">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="92d92-631">Single</span></span>                    |
| <span data-ttu-id="92d92-632">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="92d92-632">Widowed</span></span>                | <span data-ttu-id="92d92-633">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="92d92-633">Widowed</span></span>                   |
| <span data-ttu-id="92d92-634">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="92d92-634">Divorced</span></span>               | <span data-ttu-id="92d92-635">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="92d92-635">Divorced</span></span>                  |
| <span data-ttu-id="92d92-636">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="92d92-636">Registered Partnership</span></span> | <span data-ttu-id="92d92-637">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="92d92-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="92d92-638">Nėra</span><span class="sxs-lookup"><span data-stu-id="92d92-638">None</span></span>                   | <span data-ttu-id="92d92-639">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="92d92-640">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="92d92-640">Cohabiting</span></span>             | <span data-ttu-id="92d92-641">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="92d92-642">Giminė</span><span class="sxs-lookup"><span data-stu-id="92d92-642">Gender</span></span>

<span data-ttu-id="92d92-643">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="92d92-644">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="92d92-645">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-645">Human Resources</span></span>       | <span data-ttu-id="92d92-646">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="92d92-647">Vyras</span><span class="sxs-lookup"><span data-stu-id="92d92-647">Male</span></span>         | <span data-ttu-id="92d92-648">Vyras</span><span class="sxs-lookup"><span data-stu-id="92d92-648">Male</span></span>                      |
| <span data-ttu-id="92d92-649">Moteris</span><span class="sxs-lookup"><span data-stu-id="92d92-649">Female</span></span>       | <span data-ttu-id="92d92-650">Moteris</span><span class="sxs-lookup"><span data-stu-id="92d92-650">Female</span></span>                    |
| <span data-ttu-id="92d92-651">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="92d92-651">Non-specific</span></span> | <span data-ttu-id="92d92-652">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="92d92-653">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="92d92-653">Payment method</span></span>

<span data-ttu-id="92d92-654">Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="92d92-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="92d92-655">Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="92d92-656">Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="92d92-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="92d92-657">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-657">Human Resources</span></span>             | <span data-ttu-id="92d92-658">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="92d92-659">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="92d92-659">Cash</span></span>               | <span data-ttu-id="92d92-660">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="92d92-660">Cash</span></span>                      |
| <span data-ttu-id="92d92-661">Elektroninis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="92d92-661">Electronic Payment</span></span> | <span data-ttu-id="92d92-662">Perkelti</span><span class="sxs-lookup"><span data-stu-id="92d92-662">Transfer</span></span>                  |
| <span data-ttu-id="92d92-663">Tikrinti</span><span class="sxs-lookup"><span data-stu-id="92d92-663">Check</span></span>              | <span data-ttu-id="92d92-664">Čekis</span><span class="sxs-lookup"><span data-stu-id="92d92-664">Cheque</span></span>                    |
| <span data-ttu-id="92d92-665">Banko čekis</span><span class="sxs-lookup"><span data-stu-id="92d92-665">Bank Draft</span></span>         | <span data-ttu-id="92d92-666">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="92d92-667">Kiti</span><span class="sxs-lookup"><span data-stu-id="92d92-667">Other</span></span>              | <span data-ttu-id="92d92-668">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="92d92-669">Banko sąskaitos tipas</span><span class="sxs-lookup"><span data-stu-id="92d92-669">Bank account type</span></span>

<span data-ttu-id="92d92-670">Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti.</span><span class="sxs-lookup"><span data-stu-id="92d92-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="92d92-671">Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="92d92-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="92d92-672">Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="92d92-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="92d92-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-673">Human Resources</span></span>            | <span data-ttu-id="92d92-674">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="92d92-675">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-675">Checking Account</span></span>  | <span data-ttu-id="92d92-676">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-676">CheckingAccount</span></span>           |
| <span data-ttu-id="92d92-677">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-677">Payroll Account</span></span>   | <span data-ttu-id="92d92-678">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-678">PayrollAccount</span></span>            |
| <span data-ttu-id="92d92-679">Taupomoji sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-679">Savings Account</span></span>   | <span data-ttu-id="92d92-680">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="92d92-681">„BankGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-681">BankGirot account</span></span> | <span data-ttu-id="92d92-682">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="92d92-683">„PlusGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="92d92-683">PlusGirot account</span></span> | <span data-ttu-id="92d92-684">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="92d92-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="92d92-685">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="92d92-685">Earning codes</span></span>

<span data-ttu-id="92d92-686">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="92d92-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="92d92-687">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="92d92-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="92d92-688">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="92d92-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="92d92-689">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="92d92-689">Supported frequencies</span></span>

- <span data-ttu-id="92d92-690">Visos</span><span class="sxs-lookup"><span data-stu-id="92d92-690">All</span></span>
- <span data-ttu-id="92d92-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="92d92-691">EVERYPAY</span></span>
- <span data-ttu-id="92d92-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="92d92-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="92d92-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="92d92-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="92d92-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="92d92-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="92d92-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-695">1OFMTH</span></span>
- <span data-ttu-id="92d92-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-696">LASTOFMTH</span></span>
- <span data-ttu-id="92d92-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-697">2OFMTH</span></span>
- <span data-ttu-id="92d92-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-698">3OFMTH</span></span>
- <span data-ttu-id="92d92-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-699">4OFMTH</span></span>
- <span data-ttu-id="92d92-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-700">5OFMTH</span></span>
- <span data-ttu-id="92d92-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-701">1N2OFMTH</span></span>
- <span data-ttu-id="92d92-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-702">3N4OFMTH</span></span>
- <span data-ttu-id="92d92-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-703">1N3OFMTH</span></span>
- <span data-ttu-id="92d92-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-704">1N4OFMTH</span></span>
- <span data-ttu-id="92d92-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-705">2N3OFMTH</span></span>
- <span data-ttu-id="92d92-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-706">2N4OFMTH</span></span>
- <span data-ttu-id="92d92-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="92d92-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="92d92-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="92d92-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="92d92-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="92d92-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="92d92-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="92d92-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="92d92-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="92d92-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="92d92-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="92d92-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="92d92-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="92d92-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="92d92-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="92d92-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="92d92-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="92d92-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="92d92-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="92d92-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="92d92-719">Adresai</span><span class="sxs-lookup"><span data-stu-id="92d92-719">Addresses</span></span>

<span data-ttu-id="92d92-720">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="92d92-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="92d92-721">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="92d92-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="92d92-722">Personalas</span><span class="sxs-lookup"><span data-stu-id="92d92-722">Human Resources</span></span>              | <span data-ttu-id="92d92-723">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="92d92-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="92d92-724">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="92d92-724">Country/Region</span></span>      | <span data-ttu-id="92d92-725">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-725">Country Code</span></span>          |
| <span data-ttu-id="92d92-726">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-726">Zip/Postal Code</span></span>     | <span data-ttu-id="92d92-727">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="92d92-727">Postal Code</span></span>           |
| <span data-ttu-id="92d92-728">Apskritis</span><span class="sxs-lookup"><span data-stu-id="92d92-728">State</span></span>               | <span data-ttu-id="92d92-729">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="92d92-729">State Code</span></span>            |
| <span data-ttu-id="92d92-730">Miestas</span><span class="sxs-lookup"><span data-stu-id="92d92-730">City</span></span>                | <span data-ttu-id="92d92-731">Miestas</span><span class="sxs-lookup"><span data-stu-id="92d92-731">City</span></span>                  |
| <span data-ttu-id="92d92-732">Apygarda</span><span class="sxs-lookup"><span data-stu-id="92d92-732">County</span></span>              | <span data-ttu-id="92d92-733">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="92d92-733">County (Municipality)</span></span> |
| <span data-ttu-id="92d92-734">Gatvė</span><span class="sxs-lookup"><span data-stu-id="92d92-734">Street</span></span>              | <span data-ttu-id="92d92-735">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="92d92-735">Address Line 1</span></span>        |
| <span data-ttu-id="92d92-736">Gatvė, namo nr.</span><span class="sxs-lookup"><span data-stu-id="92d92-736">Street Number</span></span>       | <span data-ttu-id="92d92-737">2 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="92d92-737">Address Line 2</span></span>        |
| <span data-ttu-id="92d92-738">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="92d92-738">Building Complement</span></span> | <span data-ttu-id="92d92-739">5 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="92d92-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="92d92-740">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="92d92-740">Passport number</span></span>

<span data-ttu-id="92d92-741">Darbuotojai gali paskelbti paso informaciją.</span><span class="sxs-lookup"><span data-stu-id="92d92-741">Employees can declare passport information.</span></span> <span data-ttu-id="92d92-742">Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.</span><span class="sxs-lookup"><span data-stu-id="92d92-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="92d92-743">Identifikacijos tipas = "Pasas"</span><span class="sxs-lookup"><span data-stu-id="92d92-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="92d92-744">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-744">Issued Date</span></span>
- <span data-ttu-id="92d92-745">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="92d92-745">Expiration Date</span></span>

<span data-ttu-id="92d92-746">Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="92d92-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="92d92-747">Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas.</span><span class="sxs-lookup"><span data-stu-id="92d92-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="92d92-748">Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.</span><span class="sxs-lookup"><span data-stu-id="92d92-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]