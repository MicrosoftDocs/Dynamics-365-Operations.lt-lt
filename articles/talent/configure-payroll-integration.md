---
title: Algalapio integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti integravimą tarp „Microsoft Dynamics 365 for Talent“ ir „Ceridian Dayforce“, kad galėtumėte apdoroti mokėjimo vykdymą.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 59234ef44ad22383ae5daf71d4b663c6183e6c05
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702823"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="d9016-103">Algalapių integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d9016-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9016-104">Integravimas tarp „Microsoft Dynamics 365 for Talent“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="d9016-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="d9016-105">Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Talent“, tiek „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d9016-106">Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Talent“.</span><span class="sxs-lookup"><span data-stu-id="d9016-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="d9016-107">Integravimui reikalingi konkretūs duomenys iš „Talent“.</span><span class="sxs-lookup"><span data-stu-id="d9016-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="d9016-108">Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Talent“ taip, kad integravimas būtų palaikomas.</span><span class="sxs-lookup"><span data-stu-id="d9016-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="d9016-109">Integravimui naudojamos šios plačios duomenų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="d9016-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d9016-110">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="d9016-110">Human resources data</span></span>
- <span data-ttu-id="d9016-111">Kompensacijos duomenys</span><span class="sxs-lookup"><span data-stu-id="d9016-111">Compensation data</span></span>
- <span data-ttu-id="d9016-112">Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d9016-113">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="d9016-113">Worker data</span></span>

<span data-ttu-id="d9016-114">Šioje temoje aprašomi veiksmai, kuriuos reikia vykdyti norint įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="d9016-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d9016-115">Joje taip pat paaiškinami duomenų tipai ir išsami konfigūravimo informacija, reikalinga integravimui.</span><span class="sxs-lookup"><span data-stu-id="d9016-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d9016-116">Integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="d9016-116">Enable the integration</span></span>

<span data-ttu-id="d9016-117">Pirmiausia „Talent“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d9016-118">Jei norite, kad sukuriama didžiosios knygos operacija būtų importuota į „Microsoft Dynamics 365 for Finance and Operations“, taip pat turite sukurti „Microsoft Azure“ saugyklos paskyrą ir įvesti „Azure Storage“ jungimosi eilutę į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="d9016-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="d9016-119">Norėdami įjungti integravimą į „Talent“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d9016-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="d9016-120">Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="d9016-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d9016-121">Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.</span><span class="sxs-lookup"><span data-stu-id="d9016-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d9016-122">Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.</span><span class="sxs-lookup"><span data-stu-id="d9016-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d9016-123">Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d9016-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d9016-124">Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas.</span><span class="sxs-lookup"><span data-stu-id="d9016-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d9016-125">Galite pakeisti šį dažnumą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="d9016-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="d9016-126">Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ temose:</span><span class="sxs-lookup"><span data-stu-id="d9016-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="d9016-127">Apie „Azure“ saugyklos paskyras</span><span class="sxs-lookup"><span data-stu-id="d9016-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d9016-128">„Azure Storage“ jungimosi eilučių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d9016-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d9016-129">Techninė informacija apie algalapių integravimo įjungimą</span><span class="sxs-lookup"><span data-stu-id="d9016-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d9016-130">Įjungus algalapių integravimą gaunami du pagrindiniai rezultatai:</span><span class="sxs-lookup"><span data-stu-id="d9016-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d9016-131">Sukuriamas duomenų eksportavimo projektas pavadinimu Atlyginimų integravimo eksportavimas.</span><span class="sxs-lookup"><span data-stu-id="d9016-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d9016-132">Šiame projekte yra objektai ir laukai, kurie būtini norint užtikrinti algalapių integravimą.</span><span class="sxs-lookup"><span data-stu-id="d9016-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d9016-133">Norėdami analizuoti projektą, eikite į **Sistemos administravimas**, pasirinkite plytelę **Duomenų valdymas**, tada projektų sąraše atidarykite duomenų projektą.</span><span class="sxs-lookup"><span data-stu-id="d9016-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d9016-134">Ši paketinė užduotis vykdo duomenų eksportavimo projektą, užšifruoja gautą duomenų paketą ir perduoda duomenų paketo failą į SFTP galinį punktą, sukonfigūruotą ekrane **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="d9016-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d9016-135">Duomenų paketas, perduotas į SFTP galinį punktą, užšifruojamas naudojant unikalų pakuotės raktą.</span><span class="sxs-lookup"><span data-stu-id="d9016-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d9016-136">Raktas laikomas „Azure Key Vault“, kurį gali pasiekti tik „Ceridian“.</span><span class="sxs-lookup"><span data-stu-id="d9016-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d9016-137">Neįmanoma iššifruoti ir išanalizuoti duomenų paketo turinio.</span><span class="sxs-lookup"><span data-stu-id="d9016-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d9016-138">Jei reikia analizuoti duomenų paketo turinį, reikės rankiniu būdu eksportuoti duomenų projektą Atlyginimų integravimo eksportavimas, jį atsisiųsti ir tada atsidaryti.</span><span class="sxs-lookup"><span data-stu-id="d9016-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d9016-139">Eksportuojant rankiniu būdu nebus taikomas šifravimas ir paketas nebus perduodamas.</span><span class="sxs-lookup"><span data-stu-id="d9016-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d9016-140">Jūsų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d9016-140">Configure your data</span></span> 

<span data-ttu-id="d9016-141">Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Talent“.</span><span class="sxs-lookup"><span data-stu-id="d9016-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="d9016-142">Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir kompensacijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="d9016-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d9016-143">Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="d9016-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d9016-144">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="d9016-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d9016-145">Išmokos</span><span class="sxs-lookup"><span data-stu-id="d9016-145">Benefits</span></span> 

<span data-ttu-id="d9016-146">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų kompensacijų planus.</span><span class="sxs-lookup"><span data-stu-id="d9016-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d9016-147">Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d9016-148">Išmokų planai</span><span class="sxs-lookup"><span data-stu-id="d9016-148">Benefit plans</span></span>

- <span data-ttu-id="d9016-149">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-149">Plan (required)</span></span>
- <span data-ttu-id="d9016-150">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-150">Type (required)</span></span>
- <span data-ttu-id="d9016-151">Poveikis algalapiui (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-151">Payroll impact (required)</span></span>
- <span data-ttu-id="d9016-152">Susigrąžinti skolas</span><span class="sxs-lookup"><span data-stu-id="d9016-152">Recover arrears</span></span>
- <span data-ttu-id="d9016-153">Atskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="d9016-153">Deduction method</span></span>
- <span data-ttu-id="d9016-154">Atskaitymo pirmumas</span><span class="sxs-lookup"><span data-stu-id="d9016-154">Deduction priority</span></span>
- <span data-ttu-id="d9016-155">Apribojimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d9016-155">Limit period</span></span>
- <span data-ttu-id="d9016-156">Limito suma</span><span class="sxs-lookup"><span data-stu-id="d9016-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d9016-157">Išmokos</span><span class="sxs-lookup"><span data-stu-id="d9016-157">Benefits</span></span>

- <span data-ttu-id="d9016-158">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-158">Plan (required)</span></span>
- <span data-ttu-id="d9016-159">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-159">Type (required)</span></span>
- <span data-ttu-id="d9016-160">Parinktis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-160">Option (required)</span></span>
- <span data-ttu-id="d9016-161">Išmokos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-161">Benefit ID (required)</span></span>
- <span data-ttu-id="d9016-162">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="d9016-162">Frequency</span></span>
- <span data-ttu-id="d9016-163">Pagrindas</span><span class="sxs-lookup"><span data-stu-id="d9016-163">Basis</span></span>
- <span data-ttu-id="d9016-164">Suma arba tarifas</span><span class="sxs-lookup"><span data-stu-id="d9016-164">Amount or rate</span></span>
- <span data-ttu-id="d9016-165">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d9016-166">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="d9016-166">Supported frequencies</span></span> 

- <span data-ttu-id="d9016-167">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="d9016-167">Weekly</span></span>
- <span data-ttu-id="d9016-168">Už dvi savaites</span><span class="sxs-lookup"><span data-stu-id="d9016-168">Bi-weekly</span></span>
- <span data-ttu-id="d9016-169">Kas pusę mėnesio</span><span class="sxs-lookup"><span data-stu-id="d9016-169">Semi-monthly</span></span>
- <span data-ttu-id="d9016-170">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="d9016-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d9016-171">Palaikomos bazės</span><span class="sxs-lookup"><span data-stu-id="d9016-171">Supported bases</span></span> 

- <span data-ttu-id="d9016-172">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="d9016-172">Fixed amount</span></span>
- <span data-ttu-id="d9016-173">Pajamų procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="d9016-173">Percent of earnings</span></span>
- <span data-ttu-id="d9016-174">Produktyvios valandos</span><span class="sxs-lookup"><span data-stu-id="d9016-174">Productive hours</span></span>

<span data-ttu-id="d9016-175">„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.</span><span class="sxs-lookup"><span data-stu-id="d9016-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d9016-176">Pasirinkimas „Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-176">Selection in Talent</span></span>        | <span data-ttu-id="d9016-177">Rezultatas „Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d9016-178">None</span><span class="sxs-lookup"><span data-stu-id="d9016-178">None</span></span>                       | <span data-ttu-id="d9016-179">Nesukuriama jokio atskaitymo.</span><span class="sxs-lookup"><span data-stu-id="d9016-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="d9016-180">Tik atskaitymas</span><span class="sxs-lookup"><span data-stu-id="d9016-180">Deduction only</span></span>             | <span data-ttu-id="d9016-181">Sukuriamas darbuotojo atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="d9016-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d9016-182">Tik įnašas</span><span class="sxs-lookup"><span data-stu-id="d9016-182">Contribution only</span></span>          | <span data-ttu-id="d9016-183">Sukuriamas darbdavio atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="d9016-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d9016-184">Atskaitymas ir įnašas</span><span class="sxs-lookup"><span data-stu-id="d9016-184">Deduction and contribution</span></span> | <span data-ttu-id="d9016-185">Sukuriami darbuotojo ir darbdavio atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="d9016-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d9016-186">Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="d9016-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="d9016-187">Pristatyti darbuotojų išmokų programą</span><span class="sxs-lookup"><span data-stu-id="d9016-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d9016-188">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="d9016-188">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d9016-189">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="d9016-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d9016-190">Užregistruoti ir pašalinti išmokas darbuotojams</span><span class="sxs-lookup"><span data-stu-id="d9016-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d9016-191">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="d9016-191">Compensation</span></span> 

<span data-ttu-id="d9016-192">Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="d9016-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d9016-193">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="d9016-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d9016-194">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="d9016-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d9016-195">„Dayforce“ naudojama kompensacijos informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="d9016-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d9016-196">Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="d9016-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d9016-197">Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.</span><span class="sxs-lookup"><span data-stu-id="d9016-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d9016-198">Daugiau informacijos apie kompensacijų planus rasite šios temose:</span><span class="sxs-lookup"><span data-stu-id="d9016-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="d9016-199">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="d9016-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d9016-200">Kintamosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="d9016-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d9016-201">Kurti atlyginimų / kompensavimo struktūrą ir planus</span><span class="sxs-lookup"><span data-stu-id="d9016-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d9016-202">Kompensavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="d9016-202">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d9016-203">Kompensavimo proceso nustatymas ir rezultatų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="d9016-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d9016-204">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="d9016-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d9016-205">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="d9016-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d9016-206">Darbai</span><span class="sxs-lookup"><span data-stu-id="d9016-206">Jobs</span></span> 

<span data-ttu-id="d9016-207">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="d9016-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d9016-208">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="d9016-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d9016-209">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9016-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d9016-210">Apibrėžti naujas užduotis</span><span class="sxs-lookup"><span data-stu-id="d9016-210">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d9016-211">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="d9016-211">Positions</span></span>

<span data-ttu-id="d9016-212">Pareigos yra atskiros užduoties egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="d9016-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="d9016-213">Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="d9016-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d9016-214">Pareigos egzistuoja padalinyje.</span><span class="sxs-lookup"><span data-stu-id="d9016-214">A position exists in a department.</span></span> <span data-ttu-id="d9016-215">Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="d9016-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d9016-216">Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:</span><span class="sxs-lookup"><span data-stu-id="d9016-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d9016-217">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-217">Position (required)</span></span>
- <span data-ttu-id="d9016-218">Aprašas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-218">Description (required)</span></span>
- <span data-ttu-id="d9016-219">Užduotis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-219">Job (required)</span></span>
- <span data-ttu-id="d9016-220">Padalinys (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-220">Department (required)</span></span>
- <span data-ttu-id="d9016-221">Pareigų tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-221">Position type (required)</span></span>
- <span data-ttu-id="d9016-222">Viso etato ekvivalentas</span><span class="sxs-lookup"><span data-stu-id="d9016-222">Full-time equivalent</span></span>
- <span data-ttu-id="d9016-223">Įprastos darbo valandos per metus (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="d9016-224">Apmokama juridinio subjekto (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d9016-225">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-225">Pay cycle (required)</span></span>
- <span data-ttu-id="d9016-226">Numatytosios finansinės dimensijos – išlaidų centras (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d9016-227">Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d9016-228">Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.</span><span class="sxs-lookup"><span data-stu-id="d9016-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d9016-229">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="d9016-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d9016-230">Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas</span><span class="sxs-lookup"><span data-stu-id="d9016-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d9016-231">Pareigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9016-231">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d9016-232">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="d9016-232">Departments</span></span>

<span data-ttu-id="d9016-233">Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį.</span><span class="sxs-lookup"><span data-stu-id="d9016-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d9016-234">Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą.</span><span class="sxs-lookup"><span data-stu-id="d9016-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d9016-235">Padalinius galite naudoti norėdami pranešti apie funkcines sritis.</span><span class="sxs-lookup"><span data-stu-id="d9016-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d9016-236">Padaliniai gali turėti pelno ir nuostolio atsakomybę.</span><span class="sxs-lookup"><span data-stu-id="d9016-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d9016-237">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="d9016-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d9016-238">Padalinio kūrimas ir priskyrimas padalinių hierarchijai</span><span class="sxs-lookup"><span data-stu-id="d9016-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d9016-239">Apibrėžti naujus padalinius</span><span class="sxs-lookup"><span data-stu-id="d9016-239">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d9016-240">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="d9016-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="d9016-241">Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams.</span><span class="sxs-lookup"><span data-stu-id="d9016-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d9016-242">Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="d9016-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d9016-243">Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="d9016-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d9016-244">Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.</span><span class="sxs-lookup"><span data-stu-id="d9016-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d9016-245">Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="d9016-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d9016-246">Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="d9016-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d9016-247">Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.</span><span class="sxs-lookup"><span data-stu-id="d9016-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d9016-248">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="d9016-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d9016-249">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-249">Pay cycle (required)</span></span>
- <span data-ttu-id="d9016-250">Mokėjimo ciklo dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d9016-251">Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="d9016-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d9016-252">Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="d9016-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d9016-253">Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui.</span><span class="sxs-lookup"><span data-stu-id="d9016-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d9016-254">Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="d9016-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d9016-255">„Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Talent“.</span><span class="sxs-lookup"><span data-stu-id="d9016-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d9016-256">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-256">Earning codes</span></span>

<span data-ttu-id="d9016-257">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="d9016-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d9016-258">Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="d9016-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d9016-259">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="d9016-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d9016-260">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-260">Earning Code (required)</span></span>
- <span data-ttu-id="d9016-261">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-261">Description</span></span>
- <span data-ttu-id="d9016-262">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="d9016-262">Unit of measure</span></span>
- <span data-ttu-id="d9016-263">Produktyvus</span><span class="sxs-lookup"><span data-stu-id="d9016-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d9016-264">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="d9016-264">Worker data</span></span>

<span data-ttu-id="d9016-265">Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms.</span><span class="sxs-lookup"><span data-stu-id="d9016-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d9016-266">Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.</span><span class="sxs-lookup"><span data-stu-id="d9016-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d9016-267">Galite tvarkyti šią darbininkų informaciją:</span><span class="sxs-lookup"><span data-stu-id="d9016-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d9016-268">**Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.</span><span class="sxs-lookup"><span data-stu-id="d9016-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d9016-269">**Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="d9016-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d9016-270">**Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="d9016-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d9016-271">**Kompensacija ir algalapis** – tvarkykite informaciją apie darbininko kompensacijos planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.</span><span class="sxs-lookup"><span data-stu-id="d9016-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d9016-272">Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d9016-273">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="d9016-273">General information</span></span>

- <span data-ttu-id="d9016-274">Darbuotojo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-274">Personnel number (required)</span></span>
- <span data-ttu-id="d9016-275">Vardas (būtinas)</span><span class="sxs-lookup"><span data-stu-id="d9016-275">First name (required)</span></span>
- <span data-ttu-id="d9016-276">Pavardė (būtinai)</span><span class="sxs-lookup"><span data-stu-id="d9016-276">Last name (required)</span></span>
- <span data-ttu-id="d9016-277">Antras vardas</span><span class="sxs-lookup"><span data-stu-id="d9016-277">Middle name</span></span>
- <span data-ttu-id="d9016-278">Paaukštinimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-278">Seniority date</span></span>
- <span data-ttu-id="d9016-279">Žinoma kaip</span><span class="sxs-lookup"><span data-stu-id="d9016-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d9016-280">Asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="d9016-280">Personal information</span></span>

- <span data-ttu-id="d9016-281">Šeiminė padėtis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-281">Marital status (required)</span></span>
- <span data-ttu-id="d9016-282">Gimimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-282">Birth date (required)</span></span>
- <span data-ttu-id="d9016-283">Lytis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-283">Gender (required)</span></span>
- <span data-ttu-id="d9016-284">Asmuo su negalia</span><span class="sxs-lookup"><span data-stu-id="d9016-284">Person with disabilities</span></span>
- <span data-ttu-id="d9016-285">Pilietybės šalies regionas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="d9016-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d9016-286">Adresas</span><span class="sxs-lookup"><span data-stu-id="d9016-286">Address information</span></span>

- <span data-ttu-id="d9016-287">Pagrindinis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-287">Primary (required)</span></span>
- <span data-ttu-id="d9016-288">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-288">Country/region (required)</span></span>
- <span data-ttu-id="d9016-289">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-289">Postal code (required)</span></span>
- <span data-ttu-id="d9016-290">Gatvės numeris (būtina) (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="d9016-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d9016-291">Pastatų kompleksas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="d9016-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d9016-292">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-292">City (required)</span></span>
- <span data-ttu-id="d9016-293">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-293">State (required)</span></span>
- <span data-ttu-id="d9016-294">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d9016-295">Kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="d9016-295">Contact information</span></span> 

- <span data-ttu-id="d9016-296">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-296">Primary (required)</span></span>
- <span data-ttu-id="d9016-297">Kontakto numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-297">Contact number (required)</span></span>
- <span data-ttu-id="d9016-298">Išplėtimas</span><span class="sxs-lookup"><span data-stu-id="d9016-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d9016-299">Algalapio informacija ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-299">Payroll information and earning codes</span></span>

<span data-ttu-id="d9016-300">Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="d9016-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d9016-301">Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.</span><span class="sxs-lookup"><span data-stu-id="d9016-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d9016-302">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-302">Earning codes</span></span>

- <span data-ttu-id="d9016-303">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-303">Position (required)</span></span>
- <span data-ttu-id="d9016-304">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-304">Earning Code (required)</span></span>
- <span data-ttu-id="d9016-305">Dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-305">Frequency (required)</span></span>
- <span data-ttu-id="d9016-306">Suma (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d9016-307">Algalapių informacija</span><span class="sxs-lookup"><span data-stu-id="d9016-307">Payroll information</span></span>

- <span data-ttu-id="d9016-308">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="d9016-308">Payment Method</span></span>
- <span data-ttu-id="d9016-309">Ekonominė sritis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-309">Economic Region (required)</span></span>
- <span data-ttu-id="d9016-310">Darbuotojų išmokų ID</span><span class="sxs-lookup"><span data-stu-id="d9016-310">Employee Benefits ID</span></span>
- <span data-ttu-id="d9016-311">Asmens kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-311">National ID Number (required)</span></span>
- <span data-ttu-id="d9016-312">Karo tarnybos numeris</span><span class="sxs-lookup"><span data-stu-id="d9016-312">Military Service Number</span></span>
- <span data-ttu-id="d9016-313">Pamainos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-313">Shift ID (required)</span></span>
- <span data-ttu-id="d9016-314">Mokesčių numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-314">Tax Number (required)</span></span>
- <span data-ttu-id="d9016-315">Sąjungos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-315">Union ID (required)</span></span>
- <span data-ttu-id="d9016-316">Darbo dienos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-316">Work Day ID (required)</span></span>
- <span data-ttu-id="d9016-317">Darbo leidimo numeris</span><span class="sxs-lookup"><span data-stu-id="d9016-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d9016-318">Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="d9016-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d9016-319">Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.</span><span class="sxs-lookup"><span data-stu-id="d9016-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d9016-320">Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="d9016-320">Employment details</span></span>

<span data-ttu-id="d9016-321">Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos.</span><span class="sxs-lookup"><span data-stu-id="d9016-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d9016-322">„Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="d9016-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d9016-323">Įdarbinimo pradžios data (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-323">Employment start date (required)</span></span>
- <span data-ttu-id="d9016-324">Įdarbinimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="d9016-324">Employment end date</span></span>
- <span data-ttu-id="d9016-325">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="d9016-325">Start date</span></span>
- <span data-ttu-id="d9016-326">Patikslinta darbo pradžios data</span><span class="sxs-lookup"><span data-stu-id="d9016-326">Adjusted start date</span></span>
- <span data-ttu-id="d9016-327">Atleidimo data (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="d9016-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d9016-328">Atleidimo priežastis (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="d9016-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d9016-329">Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="d9016-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d9016-330">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-330">Talent</span></span>                | <span data-ttu-id="d9016-331">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9016-332">Naujausia samdos data</span><span class="sxs-lookup"><span data-stu-id="d9016-332">Most recent hire date</span></span> | <span data-ttu-id="d9016-333">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="d9016-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d9016-334">Atleidimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-334">Termination date</span></span>      | <span data-ttu-id="d9016-335">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d9016-336">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="d9016-336">Start date</span></span>            | <span data-ttu-id="d9016-337">Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="d9016-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d9016-338">Pradinio įdarbinimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-338">Original hire date</span></span>    | <span data-ttu-id="d9016-339">Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="d9016-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d9016-340">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="d9016-340">Compensation</span></span>

<span data-ttu-id="d9016-341">Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="d9016-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d9016-342">Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d9016-343">Įsigaliojimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-343">Effective Date (required)</span></span>
- <span data-ttu-id="d9016-344">Galiojimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="d9016-344">Expiration date</span></span>
- <span data-ttu-id="d9016-345">Užmokesčio tarifas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-345">Pay Rate (required)</span></span>
- <span data-ttu-id="d9016-346">Užmokesčio tarifo konvertavimas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d9016-347">Metinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="d9016-348">Valandinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="d9016-349">Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="d9016-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d9016-350">Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d9016-351">Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="d9016-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d9016-352">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="d9016-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d9016-353">Socialinio draudimo identifikatorius</span><span class="sxs-lookup"><span data-stu-id="d9016-353">Social Security identifier</span></span> 

<span data-ttu-id="d9016-354">Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="d9016-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d9016-355">Šis identifikatorius turi būti **SSN** identifikacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="d9016-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d9016-356">„Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.</span><span class="sxs-lookup"><span data-stu-id="d9016-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d9016-357">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-357">Primary (required)</span></span>
- <span data-ttu-id="d9016-358">Identifikacijos tipas = "SSN"</span><span class="sxs-lookup"><span data-stu-id="d9016-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d9016-359">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-359">Issued Date</span></span>
- <span data-ttu-id="d9016-360">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-360">Expiration Date</span></span>

<span data-ttu-id="d9016-361">Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="d9016-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d9016-362">Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.</span><span class="sxs-lookup"><span data-stu-id="d9016-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d9016-363">Banko sąskaitos ir išmokos</span><span class="sxs-lookup"><span data-stu-id="d9016-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="d9016-364">Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="d9016-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d9016-365">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-365">Talent</span></span>                         | <span data-ttu-id="d9016-366">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9016-367">Banko sąskaitos numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d9016-368">SWIFT kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-368">SWIFT code (required)</span></span>          | <span data-ttu-id="d9016-369">**Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="d9016-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d9016-370">Filialo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d9016-371">Banko sąskaitos tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-371">Bank account type (required)</span></span>   | <span data-ttu-id="d9016-372">**Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="d9016-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d9016-373">Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**.</span><span class="sxs-lookup"><span data-stu-id="d9016-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d9016-374">Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke.</span><span class="sxs-lookup"><span data-stu-id="d9016-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d9016-375">Visos kitos nelikutinės sąskaitos yra ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="d9016-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d9016-376">Adresas</span><span class="sxs-lookup"><span data-stu-id="d9016-376">Address information</span></span>

<span data-ttu-id="d9016-377">Kiekvienas darbuotojas turi turėti vieną pirminę vietą.</span><span class="sxs-lookup"><span data-stu-id="d9016-377">Every employee must have one primary location.</span></span> <span data-ttu-id="d9016-378">„Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.</span><span class="sxs-lookup"><span data-stu-id="d9016-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d9016-379">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-379">Primary (required)</span></span>
- <span data-ttu-id="d9016-380">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-380">Country/region (required)</span></span>
- <span data-ttu-id="d9016-381">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="d9016-382">Gatvė (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-382">Street (required)</span></span>
- <span data-ttu-id="d9016-383">Gatvės numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-383">Street Number (required)</span></span>
- <span data-ttu-id="d9016-384">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="d9016-384">Building Complement</span></span>
- <span data-ttu-id="d9016-385">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-385">City (required)</span></span>
- <span data-ttu-id="d9016-386">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-386">State (required)</span></span>
- <span data-ttu-id="d9016-387">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d9016-388">Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje</span><span class="sxs-lookup"><span data-stu-id="d9016-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d9016-389">Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="d9016-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d9016-390">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="d9016-390">Departments are required on positions.</span></span>
- <span data-ttu-id="d9016-391">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d9016-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d9016-392">Galite sukonfigūruoti „Talent“, kad prie pareigų būtų nurodytas padalinys.</span><span class="sxs-lookup"><span data-stu-id="d9016-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="d9016-393">Norėdami tai atlikti, eikite į **Bendrinamos personalo pareigos > Pareigos > Prie pareigų reikalauti padalinių**.</span><span class="sxs-lookup"><span data-stu-id="d9016-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d9016-394">Rekomenduojame integruojant šį parametrą taikyti.</span><span class="sxs-lookup"><span data-stu-id="d9016-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d9016-395">Pareigų rūšys</span><span class="sxs-lookup"><span data-stu-id="d9016-395">Job types</span></span>

<span data-ttu-id="d9016-396">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="d9016-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d9016-397">Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje.</span><span class="sxs-lookup"><span data-stu-id="d9016-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d9016-398">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="d9016-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d9016-399">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="d9016-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d9016-400">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d9016-401">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="d9016-401">Job type</span></span>   | <span data-ttu-id="d9016-402">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d9016-403">Valandinis</span><span class="sxs-lookup"><span data-stu-id="d9016-403">Hourly</span></span>     | <span data-ttu-id="d9016-404">Valandinis</span><span class="sxs-lookup"><span data-stu-id="d9016-404">Hourly</span></span>      |
| <span data-ttu-id="d9016-405">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="d9016-405">Salaried</span></span>   | <span data-ttu-id="d9016-406">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="d9016-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d9016-407">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="d9016-407">Position types</span></span> 

<span data-ttu-id="d9016-408">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="d9016-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d9016-409">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="d9016-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d9016-410">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d9016-411">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="d9016-411">Position type</span></span>   | <span data-ttu-id="d9016-412">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d9016-413">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-413">Full-time</span></span>       | <span data-ttu-id="d9016-414">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-414">Full time employee</span></span> |
| <span data-ttu-id="d9016-415">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-415">Part-time</span></span>       | <span data-ttu-id="d9016-416">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d9016-417">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-417">Reason codes</span></span>

<span data-ttu-id="d9016-418">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="d9016-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d9016-419">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="d9016-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d9016-420">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d9016-421">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="d9016-421">Reason code</span></span>    | <span data-ttu-id="d9016-422">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-422">Description</span></span>      | <span data-ttu-id="d9016-423">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="d9016-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d9016-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d9016-424">RESIGNATION</span></span>    | <span data-ttu-id="d9016-425">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="d9016-425">Resignation</span></span>      | <span data-ttu-id="d9016-426">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-426">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d9016-427">TERMINATION</span></span>    | <span data-ttu-id="d9016-428">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="d9016-428">Termination</span></span>      | <span data-ttu-id="d9016-429">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-429">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d9016-430">RETIREMENT</span></span>     | <span data-ttu-id="d9016-431">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="d9016-431">Retirement</span></span>       | <span data-ttu-id="d9016-432">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-432">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-433">KITA</span><span class="sxs-lookup"><span data-stu-id="d9016-433">OTHER</span></span>          | <span data-ttu-id="d9016-434">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="d9016-434">Other Reasons</span></span>    | <span data-ttu-id="d9016-435">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-435">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="d9016-436">DEATH</span></span>          | <span data-ttu-id="d9016-437">Mirtis</span><span class="sxs-lookup"><span data-stu-id="d9016-437">Death</span></span>            | <span data-ttu-id="d9016-438">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-438">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d9016-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d9016-440">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="d9016-440">Leave of Absence</span></span> | <span data-ttu-id="d9016-441">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-441">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d9016-442">CONTRACTEND</span></span>    | <span data-ttu-id="d9016-443">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="d9016-443">End of Contract</span></span>  | <span data-ttu-id="d9016-444">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-444">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d9016-445">SALARYCHANGE</span></span>   | <span data-ttu-id="d9016-446">Atlyginimo pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="d9016-446">Change of Salary</span></span> | <span data-ttu-id="d9016-447">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="d9016-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d9016-448">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="d9016-448">Marital status</span></span>

<span data-ttu-id="d9016-449">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d9016-450">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d9016-451">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-451">Talent</span></span>                 | <span data-ttu-id="d9016-452">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d9016-453">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-453">Married</span></span>                | <span data-ttu-id="d9016-454">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-454">Married</span></span>              |
| <span data-ttu-id="d9016-455">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-455">Single</span></span>                 | <span data-ttu-id="d9016-456">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-456">Single</span></span>               |
| <span data-ttu-id="d9016-457">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="d9016-457">Widowed</span></span>                | <span data-ttu-id="d9016-458">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="d9016-458">Widowed</span></span>              |
| <span data-ttu-id="d9016-459">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="d9016-459">Divorced</span></span>               | <span data-ttu-id="d9016-460">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="d9016-460">Divorced</span></span>             |
| <span data-ttu-id="d9016-461">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="d9016-461">Registered Partnership</span></span> | <span data-ttu-id="d9016-462">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="d9016-462">Domestic Partnership</span></span> |
| <span data-ttu-id="d9016-463">None</span><span class="sxs-lookup"><span data-stu-id="d9016-463">None</span></span>                   | <span data-ttu-id="d9016-464">None</span><span class="sxs-lookup"><span data-stu-id="d9016-464">None</span></span>                 |
| <span data-ttu-id="d9016-465">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="d9016-465">Cohabiting</span></span>             | <span data-ttu-id="d9016-466">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="d9016-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d9016-467">Giminė</span><span class="sxs-lookup"><span data-stu-id="d9016-467">Gender</span></span>

<span data-ttu-id="d9016-468">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d9016-469">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d9016-470">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-470">Talent</span></span>       | <span data-ttu-id="d9016-471">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d9016-472">Vyras</span><span class="sxs-lookup"><span data-stu-id="d9016-472">Male</span></span>         | <span data-ttu-id="d9016-473">Vyras</span><span class="sxs-lookup"><span data-stu-id="d9016-473">Male</span></span>            |
| <span data-ttu-id="d9016-474">Moteris</span><span class="sxs-lookup"><span data-stu-id="d9016-474">Female</span></span>       | <span data-ttu-id="d9016-475">Moteris</span><span class="sxs-lookup"><span data-stu-id="d9016-475">Female</span></span>          |
| <span data-ttu-id="d9016-476">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="d9016-476">Non-specific</span></span> | <span data-ttu-id="d9016-477">*Nepalaikoma*</span><span class="sxs-lookup"><span data-stu-id="d9016-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d9016-478">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-478">Earning codes</span></span>

<span data-ttu-id="d9016-479">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="d9016-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d9016-480">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="d9016-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d9016-481">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="d9016-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d9016-482">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="d9016-482">Supported frequencies</span></span>

- <span data-ttu-id="d9016-483">Visos</span><span class="sxs-lookup"><span data-stu-id="d9016-483">All</span></span>
- <span data-ttu-id="d9016-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d9016-484">EVERYPAY</span></span>
- <span data-ttu-id="d9016-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d9016-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d9016-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d9016-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d9016-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d9016-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d9016-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-488">1OFMTH</span></span>
- <span data-ttu-id="d9016-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-489">LASTOFMTH</span></span>
- <span data-ttu-id="d9016-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-490">2OFMTH</span></span>
- <span data-ttu-id="d9016-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-491">3OFMTH</span></span>
- <span data-ttu-id="d9016-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-492">4OFMTH</span></span>
- <span data-ttu-id="d9016-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-493">5OFMTH</span></span>
- <span data-ttu-id="d9016-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-494">1N2OFMTH</span></span>
- <span data-ttu-id="d9016-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-495">3N4OFMTH</span></span>
- <span data-ttu-id="d9016-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-496">1N3OFMTH</span></span>
- <span data-ttu-id="d9016-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-497">1N4OFMTH</span></span>
- <span data-ttu-id="d9016-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-498">2N3OFMTH</span></span>
- <span data-ttu-id="d9016-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-499">2N4OFMTH</span></span>
- <span data-ttu-id="d9016-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="d9016-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="d9016-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="d9016-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="d9016-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d9016-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d9016-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d9016-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d9016-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d9016-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d9016-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d9016-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d9016-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d9016-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d9016-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d9016-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d9016-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d9016-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d9016-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d9016-512">Adresai</span><span class="sxs-lookup"><span data-stu-id="d9016-512">Addresses</span></span>

<span data-ttu-id="d9016-513">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="d9016-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d9016-514">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="d9016-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d9016-515">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-515">Talent</span></span>          | <span data-ttu-id="d9016-516">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d9016-517">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="d9016-517">Country/Region</span></span>  | <span data-ttu-id="d9016-518">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-518">Country Code</span></span>          |
| <span data-ttu-id="d9016-519">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-519">Zip/Postal Code</span></span> | <span data-ttu-id="d9016-520">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="d9016-520">Postal Code</span></span>           |
| <span data-ttu-id="d9016-521">Apskritis</span><span class="sxs-lookup"><span data-stu-id="d9016-521">State</span></span>           | <span data-ttu-id="d9016-522">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-522">State Code</span></span>            |
| <span data-ttu-id="d9016-523">Miestas</span><span class="sxs-lookup"><span data-stu-id="d9016-523">City</span></span>            | <span data-ttu-id="d9016-524">Miestas</span><span class="sxs-lookup"><span data-stu-id="d9016-524">City</span></span>                  |
| <span data-ttu-id="d9016-525">Apygarda</span><span class="sxs-lookup"><span data-stu-id="d9016-525">County</span></span>          | <span data-ttu-id="d9016-526">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="d9016-526">County (Municipality)</span></span> |
| <span data-ttu-id="d9016-527">Gatvė</span><span class="sxs-lookup"><span data-stu-id="d9016-527">Street</span></span>          | <span data-ttu-id="d9016-528">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="d9016-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d9016-529">Mokesčių regionai</span><span class="sxs-lookup"><span data-stu-id="d9016-529">Tax regions</span></span>

<span data-ttu-id="d9016-530">Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį.</span><span class="sxs-lookup"><span data-stu-id="d9016-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d9016-531">Mokesčių regionai yra susieti su „Dayforce“ vietų adresais.</span><span class="sxs-lookup"><span data-stu-id="d9016-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d9016-532">Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis.</span><span class="sxs-lookup"><span data-stu-id="d9016-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d9016-533">Mokesčių regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-533">Tax region (required)</span></span>
- <span data-ttu-id="d9016-534">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-534">Country/Region (required)</span></span>
- <span data-ttu-id="d9016-535">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-535">State (required)</span></span>
- <span data-ttu-id="d9016-536">Apygarda</span><span class="sxs-lookup"><span data-stu-id="d9016-536">County</span></span> 
- <span data-ttu-id="d9016-537">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="d9016-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d9016-538">Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje</span><span class="sxs-lookup"><span data-stu-id="d9016-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d9016-539">Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="d9016-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d9016-540">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="d9016-540">Departments are required on positions.</span></span>
- <span data-ttu-id="d9016-541">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d9016-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d9016-542">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="d9016-542">Job types</span></span>

<span data-ttu-id="d9016-543">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="d9016-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d9016-544">Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="d9016-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d9016-545">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="d9016-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d9016-546">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="d9016-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d9016-547">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d9016-548">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="d9016-548">Job type</span></span>   | <span data-ttu-id="d9016-549">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d9016-550">Valandinis</span><span class="sxs-lookup"><span data-stu-id="d9016-550">Hourly</span></span>     | <span data-ttu-id="d9016-551">MX valandinis</span><span class="sxs-lookup"><span data-stu-id="d9016-551">MX Hourly</span></span>   |
| <span data-ttu-id="d9016-552">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="d9016-552">Salaried</span></span>   | <span data-ttu-id="d9016-553">MX fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="d9016-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d9016-554">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="d9016-554">Position types</span></span> 

<span data-ttu-id="d9016-555">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="d9016-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d9016-556">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="d9016-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d9016-557">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d9016-558">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="d9016-558">Position type</span></span>   | <span data-ttu-id="d9016-559">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d9016-560">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-560">Full-time</span></span>       | <span data-ttu-id="d9016-561">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-561">Full time employee</span></span> |
| <span data-ttu-id="d9016-562">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-562">Part-time</span></span>       | <span data-ttu-id="d9016-563">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="d9016-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d9016-564">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-564">Reason codes</span></span>

<span data-ttu-id="d9016-565">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="d9016-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d9016-566">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="d9016-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d9016-567">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d9016-568">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="d9016-568">Reason code</span></span>            | <span data-ttu-id="d9016-569">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-569">Description</span></span>                    | <span data-ttu-id="d9016-570">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="d9016-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d9016-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d9016-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d9016-572">Išvykimas prieš pirmą algalapį</span><span class="sxs-lookup"><span data-stu-id="d9016-572">Departure before first payroll</span></span> | <span data-ttu-id="d9016-573">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-573">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d9016-574">RESIGNATION</span></span>            | <span data-ttu-id="d9016-575">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="d9016-575">Resignation</span></span>                    | <span data-ttu-id="d9016-576">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-576">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="d9016-577">PENSION</span></span>                | <span data-ttu-id="d9016-578">Pensija</span><span class="sxs-lookup"><span data-stu-id="d9016-578">Pension</span></span>                        | <span data-ttu-id="d9016-579">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-579">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d9016-580">TERMINATION</span></span>            | <span data-ttu-id="d9016-581">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="d9016-581">Termination</span></span>                    | <span data-ttu-id="d9016-582">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-582">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d9016-583">RETIREMENT</span></span>             | <span data-ttu-id="d9016-584">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="d9016-584">Retirement</span></span>                     | <span data-ttu-id="d9016-585">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-585">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d9016-586">ABSENTEE</span></span>               | <span data-ttu-id="d9016-587">Nesantysis</span><span class="sxs-lookup"><span data-stu-id="d9016-587">Absentee</span></span>                       | <span data-ttu-id="d9016-588">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-588">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-589">KITA</span><span class="sxs-lookup"><span data-stu-id="d9016-589">OTHER</span></span>                  | <span data-ttu-id="d9016-590">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="d9016-590">Other Reasons</span></span>                  | <span data-ttu-id="d9016-591">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-591">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="d9016-592">CLOSURE</span></span>                | <span data-ttu-id="d9016-593">Įmonės uždarymas</span><span class="sxs-lookup"><span data-stu-id="d9016-593">Business Closure</span></span>               | <span data-ttu-id="d9016-594">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-594">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="d9016-595">DEATH</span></span>                  | <span data-ttu-id="d9016-596">Mirtis</span><span class="sxs-lookup"><span data-stu-id="d9016-596">Death</span></span>                          | <span data-ttu-id="d9016-597">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-597">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d9016-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d9016-599">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="d9016-599">Leave of Absence</span></span>               | <span data-ttu-id="d9016-600">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-600">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d9016-601">CONTRACTEND</span></span>            | <span data-ttu-id="d9016-602">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="d9016-602">End of Contract</span></span>                | <span data-ttu-id="d9016-603">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="d9016-603">Terminate worker</span></span>     |
| <span data-ttu-id="d9016-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d9016-604">SALARYCHANGE</span></span>           | <span data-ttu-id="d9016-605">Atlyginimo keitimas</span><span class="sxs-lookup"><span data-stu-id="d9016-605">Change of Salary</span></span>               | <span data-ttu-id="d9016-606">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="d9016-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d9016-607">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="d9016-607">Terms of employment</span></span>

<span data-ttu-id="d9016-608">Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="d9016-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d9016-609">Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.</span><span class="sxs-lookup"><span data-stu-id="d9016-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d9016-610">Šios įdarbinimo sąlygos ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="d9016-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d9016-611">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="d9016-611">Terms of employment</span></span>   | <span data-ttu-id="d9016-612">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d9016-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d9016-613">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="d9016-613">Regular</span></span>               | <span data-ttu-id="d9016-614">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="d9016-614">Regular</span></span>     |
| <span data-ttu-id="d9016-615">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="d9016-615">Direct</span></span>                | <span data-ttu-id="d9016-616">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="d9016-616">Direct</span></span>      |
| <span data-ttu-id="d9016-617">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="d9016-617">Internship</span></span>            | <span data-ttu-id="d9016-618">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="d9016-618">Internship</span></span>  |
| <span data-ttu-id="d9016-619">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="d9016-619">Permanent</span></span>             | <span data-ttu-id="d9016-620">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="d9016-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d9016-621">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="d9016-621">Marital status</span></span>

<span data-ttu-id="d9016-622">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d9016-623">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d9016-624">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-624">Talent</span></span>                 | <span data-ttu-id="d9016-625">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d9016-626">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-626">Married</span></span>                | <span data-ttu-id="d9016-627">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-627">Married</span></span>                   |
| <span data-ttu-id="d9016-628">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-628">Single</span></span>                 | <span data-ttu-id="d9016-629">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="d9016-629">Single</span></span>                    |
| <span data-ttu-id="d9016-630">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="d9016-630">Widowed</span></span>                | <span data-ttu-id="d9016-631">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="d9016-631">Widowed</span></span>                   |
| <span data-ttu-id="d9016-632">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="d9016-632">Divorced</span></span>               | <span data-ttu-id="d9016-633">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="d9016-633">Divorced</span></span>                  |
| <span data-ttu-id="d9016-634">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="d9016-634">Registered Partnership</span></span> | <span data-ttu-id="d9016-635">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="d9016-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="d9016-636">None</span><span class="sxs-lookup"><span data-stu-id="d9016-636">None</span></span>                   | <span data-ttu-id="d9016-637">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d9016-638">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="d9016-638">Cohabiting</span></span>             | <span data-ttu-id="d9016-639">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d9016-640">Giminė</span><span class="sxs-lookup"><span data-stu-id="d9016-640">Gender</span></span>

<span data-ttu-id="d9016-641">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d9016-642">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d9016-643">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-643">Talent</span></span>       | <span data-ttu-id="d9016-644">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d9016-645">Vyras</span><span class="sxs-lookup"><span data-stu-id="d9016-645">Male</span></span>         | <span data-ttu-id="d9016-646">Vyras</span><span class="sxs-lookup"><span data-stu-id="d9016-646">Male</span></span>                      |
| <span data-ttu-id="d9016-647">Moteris</span><span class="sxs-lookup"><span data-stu-id="d9016-647">Female</span></span>       | <span data-ttu-id="d9016-648">Moteris</span><span class="sxs-lookup"><span data-stu-id="d9016-648">Female</span></span>                    |
| <span data-ttu-id="d9016-649">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="d9016-649">Non-specific</span></span> | <span data-ttu-id="d9016-650">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d9016-651">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="d9016-651">Payment method</span></span>

<span data-ttu-id="d9016-652">Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="d9016-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d9016-653">Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d9016-654">Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="d9016-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d9016-655">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-655">Talent</span></span>             | <span data-ttu-id="d9016-656">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d9016-657">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="d9016-657">Cash</span></span>               | <span data-ttu-id="d9016-658">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="d9016-658">Cash</span></span>                      |
| <span data-ttu-id="d9016-659">Elektroninis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="d9016-659">Electronic Payment</span></span> | <span data-ttu-id="d9016-660">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="d9016-660">Transfer</span></span>                  |
| <span data-ttu-id="d9016-661">Tikrinti</span><span class="sxs-lookup"><span data-stu-id="d9016-661">Check</span></span>              | <span data-ttu-id="d9016-662">Čekis</span><span class="sxs-lookup"><span data-stu-id="d9016-662">Cheque</span></span>                    |
| <span data-ttu-id="d9016-663">Banko čekis</span><span class="sxs-lookup"><span data-stu-id="d9016-663">Bank Draft</span></span>         | <span data-ttu-id="d9016-664">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d9016-665">Kiti</span><span class="sxs-lookup"><span data-stu-id="d9016-665">Other</span></span>              | <span data-ttu-id="d9016-666">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d9016-667">Banko sąskaitos tipas</span><span class="sxs-lookup"><span data-stu-id="d9016-667">Bank account type</span></span>

<span data-ttu-id="d9016-668">Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d9016-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d9016-669">Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="d9016-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d9016-670">Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="d9016-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d9016-671">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-671">Talent</span></span>            | <span data-ttu-id="d9016-672">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d9016-673">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-673">Checking Account</span></span>  | <span data-ttu-id="d9016-674">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-674">CheckingAccount</span></span>           |
| <span data-ttu-id="d9016-675">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-675">Payroll Account</span></span>   | <span data-ttu-id="d9016-676">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-676">PayrollAccount</span></span>            |
| <span data-ttu-id="d9016-677">Taupomoji sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-677">Savings Account</span></span>   | <span data-ttu-id="d9016-678">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d9016-679">„BankGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-679">BankGirot account</span></span> | <span data-ttu-id="d9016-680">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d9016-681">„PlusGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="d9016-681">PlusGirot account</span></span> | <span data-ttu-id="d9016-682">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="d9016-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d9016-683">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="d9016-683">Earning codes</span></span>

<span data-ttu-id="d9016-684">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="d9016-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d9016-685">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="d9016-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d9016-686">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="d9016-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d9016-687">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="d9016-687">Supported frequencies</span></span>

- <span data-ttu-id="d9016-688">Visos</span><span class="sxs-lookup"><span data-stu-id="d9016-688">All</span></span>
- <span data-ttu-id="d9016-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d9016-689">EVERYPAY</span></span>
- <span data-ttu-id="d9016-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d9016-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d9016-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d9016-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d9016-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d9016-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d9016-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-693">1OFMTH</span></span>
- <span data-ttu-id="d9016-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-694">LASTOFMTH</span></span>
- <span data-ttu-id="d9016-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-695">2OFMTH</span></span>
- <span data-ttu-id="d9016-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-696">3OFMTH</span></span>
- <span data-ttu-id="d9016-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-697">4OFMTH</span></span>
- <span data-ttu-id="d9016-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-698">5OFMTH</span></span>
- <span data-ttu-id="d9016-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-699">1N2OFMTH</span></span>
- <span data-ttu-id="d9016-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-700">3N4OFMTH</span></span>
- <span data-ttu-id="d9016-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-701">1N3OFMTH</span></span>
- <span data-ttu-id="d9016-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-702">1N4OFMTH</span></span>
- <span data-ttu-id="d9016-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-703">2N3OFMTH</span></span>
- <span data-ttu-id="d9016-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-704">2N4OFMTH</span></span>
- <span data-ttu-id="d9016-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="d9016-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="d9016-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="d9016-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="d9016-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d9016-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d9016-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d9016-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d9016-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d9016-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d9016-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d9016-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d9016-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d9016-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d9016-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d9016-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d9016-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d9016-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d9016-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d9016-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d9016-717">Adresai</span><span class="sxs-lookup"><span data-stu-id="d9016-717">Addresses</span></span>

<span data-ttu-id="d9016-718">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="d9016-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d9016-719">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="d9016-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d9016-720">„Talent“</span><span class="sxs-lookup"><span data-stu-id="d9016-720">Talent</span></span>              | <span data-ttu-id="d9016-721">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="d9016-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d9016-722">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="d9016-722">Country/Region</span></span>      | <span data-ttu-id="d9016-723">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-723">Country Code</span></span>          |
| <span data-ttu-id="d9016-724">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-724">Zip/Postal Code</span></span>     | <span data-ttu-id="d9016-725">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="d9016-725">Postal Code</span></span>           |
| <span data-ttu-id="d9016-726">Apskritis</span><span class="sxs-lookup"><span data-stu-id="d9016-726">State</span></span>               | <span data-ttu-id="d9016-727">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="d9016-727">State Code</span></span>            |
| <span data-ttu-id="d9016-728">Miestas</span><span class="sxs-lookup"><span data-stu-id="d9016-728">City</span></span>                | <span data-ttu-id="d9016-729">Miestas</span><span class="sxs-lookup"><span data-stu-id="d9016-729">City</span></span>                  |
| <span data-ttu-id="d9016-730">Apygarda</span><span class="sxs-lookup"><span data-stu-id="d9016-730">County</span></span>              | <span data-ttu-id="d9016-731">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="d9016-731">County (Municipality)</span></span> |
| <span data-ttu-id="d9016-732">Gatvė</span><span class="sxs-lookup"><span data-stu-id="d9016-732">Street</span></span>              | <span data-ttu-id="d9016-733">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="d9016-733">Address Line 1</span></span>        |
| <span data-ttu-id="d9016-734">Gatvė, namo nr.</span><span class="sxs-lookup"><span data-stu-id="d9016-734">Street Number</span></span>       | <span data-ttu-id="d9016-735">2 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="d9016-735">Address Line 2</span></span>        |
| <span data-ttu-id="d9016-736">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="d9016-736">Building Complement</span></span> | <span data-ttu-id="d9016-737">5 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="d9016-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d9016-738">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="d9016-738">Passport number</span></span>

<span data-ttu-id="d9016-739">Darbuotojai gali paskelbti paso informaciją.</span><span class="sxs-lookup"><span data-stu-id="d9016-739">Employees can declare passport information.</span></span> <span data-ttu-id="d9016-740">Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.</span><span class="sxs-lookup"><span data-stu-id="d9016-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d9016-741">Identifikacijos tipas = "Pasas"</span><span class="sxs-lookup"><span data-stu-id="d9016-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d9016-742">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-742">Issued Date</span></span>
- <span data-ttu-id="d9016-743">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="d9016-743">Expiration Date</span></span>

<span data-ttu-id="d9016-744">Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="d9016-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d9016-745">Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas.</span><span class="sxs-lookup"><span data-stu-id="d9016-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d9016-746">Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.</span><span class="sxs-lookup"><span data-stu-id="d9016-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
