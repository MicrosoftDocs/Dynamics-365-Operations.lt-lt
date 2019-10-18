---
title: Algalapio integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti integravimą tarp „Microsoft Dynamics 365 Talent“ ir „Ceridian Dayforce“, kad galėtumėte apdoroti mokėjimo vykdymą.
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
ms.openlocfilehash: ec1d14cb14ab709dfc1bead4be0785904efcce4e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251044"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="66c93-103">Algalapių integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="66c93-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66c93-104">Integravimas tarp „Microsoft Dynamics 365 Talent“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="66c93-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="66c93-105">Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Talent“, tiek „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="66c93-106">Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Talent“.</span><span class="sxs-lookup"><span data-stu-id="66c93-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="66c93-107">Integravimui reikalingi konkretūs duomenys iš „Talent“.</span><span class="sxs-lookup"><span data-stu-id="66c93-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="66c93-108">Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Talent“ taip, kad integravimas būtų palaikomas.</span><span class="sxs-lookup"><span data-stu-id="66c93-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="66c93-109">Integravimui naudojamos šios plačios duomenų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="66c93-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="66c93-110">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="66c93-110">Human resources data</span></span>
- <span data-ttu-id="66c93-111">Kompensacijos duomenys</span><span class="sxs-lookup"><span data-stu-id="66c93-111">Compensation data</span></span>
- <span data-ttu-id="66c93-112">Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="66c93-113">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="66c93-113">Worker data</span></span>

<span data-ttu-id="66c93-114">Šioje temoje aprašomi veiksmai, kuriuos reikia vykdyti norint įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="66c93-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="66c93-115">Joje taip pat paaiškinami duomenų tipai ir išsami konfigūravimo informacija, reikalinga integravimui.</span><span class="sxs-lookup"><span data-stu-id="66c93-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="66c93-116">Integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="66c93-116">Enable the integration</span></span>

<span data-ttu-id="66c93-117">Pirmiausia „Talent“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="66c93-118">Jei norite, kad sukuriama didžiosios knygos operacija būtų importuota į „Microsoft Dynamics 365 Finance“, taip pat turite sukurti „Microsoft Azure“ saugyklos paskyrą ir įvesti „Azure Storage“ jungimosi eilutę į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="66c93-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="66c93-119">Norėdami įjungti integravimą į „Talent“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="66c93-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="66c93-120">Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="66c93-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="66c93-121">Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.</span><span class="sxs-lookup"><span data-stu-id="66c93-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="66c93-122">Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.</span><span class="sxs-lookup"><span data-stu-id="66c93-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="66c93-123">Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="66c93-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="66c93-124">Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas.</span><span class="sxs-lookup"><span data-stu-id="66c93-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="66c93-125">Galite pakeisti šį dažnumą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="66c93-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="66c93-126">Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ temose:</span><span class="sxs-lookup"><span data-stu-id="66c93-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="66c93-127">Apie „Azure“ saugyklos paskyras</span><span class="sxs-lookup"><span data-stu-id="66c93-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="66c93-128">„Azure Storage“ jungimosi eilučių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="66c93-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="66c93-129">Techninė informacija apie algalapių integravimo įjungimą</span><span class="sxs-lookup"><span data-stu-id="66c93-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="66c93-130">Įjungus algalapių integravimą gaunami du pagrindiniai rezultatai:</span><span class="sxs-lookup"><span data-stu-id="66c93-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="66c93-131">Sukuriamas duomenų eksportavimo projektas pavadinimu Atlyginimų integravimo eksportavimas.</span><span class="sxs-lookup"><span data-stu-id="66c93-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="66c93-132">Šiame projekte yra objektai ir laukai, kurie būtini norint užtikrinti algalapių integravimą.</span><span class="sxs-lookup"><span data-stu-id="66c93-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="66c93-133">Norėdami analizuoti projektą, eikite į **Sistemos administravimas**, pasirinkite plytelę **Duomenų valdymas**, tada projektų sąraše atidarykite duomenų projektą.</span><span class="sxs-lookup"><span data-stu-id="66c93-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="66c93-134">Ši paketinė užduotis vykdo duomenų eksportavimo projektą, užšifruoja gautą duomenų paketą ir perduoda duomenų paketo failą į SFTP galinį punktą, sukonfigūruotą ekrane **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="66c93-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="66c93-135">Duomenų paketas, perduotas į SFTP galinį punktą, užšifruojamas naudojant unikalų pakuotės raktą.</span><span class="sxs-lookup"><span data-stu-id="66c93-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="66c93-136">Raktas laikomas „Azure Key Vault“, kurį gali pasiekti tik „Ceridian“.</span><span class="sxs-lookup"><span data-stu-id="66c93-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="66c93-137">Neįmanoma iššifruoti ir išanalizuoti duomenų paketo turinio.</span><span class="sxs-lookup"><span data-stu-id="66c93-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="66c93-138">Jei reikia analizuoti duomenų paketo turinį, reikės rankiniu būdu eksportuoti duomenų projektą Atlyginimų integravimo eksportavimas, jį atsisiųsti ir tada atsidaryti.</span><span class="sxs-lookup"><span data-stu-id="66c93-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="66c93-139">Eksportuojant rankiniu būdu nebus taikomas šifravimas ir paketas nebus perduodamas.</span><span class="sxs-lookup"><span data-stu-id="66c93-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="66c93-140">Jūsų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="66c93-140">Configure your data</span></span> 

<span data-ttu-id="66c93-141">Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Talent“.</span><span class="sxs-lookup"><span data-stu-id="66c93-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="66c93-142">Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir kompensacijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="66c93-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="66c93-143">Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="66c93-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="66c93-144">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="66c93-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="66c93-145">Išmokos</span><span class="sxs-lookup"><span data-stu-id="66c93-145">Benefits</span></span> 

<span data-ttu-id="66c93-146">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų kompensacijų planus.</span><span class="sxs-lookup"><span data-stu-id="66c93-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="66c93-147">Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="66c93-148">Išmokų planai</span><span class="sxs-lookup"><span data-stu-id="66c93-148">Benefit plans</span></span>

- <span data-ttu-id="66c93-149">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-149">Plan (required)</span></span>
- <span data-ttu-id="66c93-150">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-150">Type (required)</span></span>
- <span data-ttu-id="66c93-151">Poveikis algalapiui (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-151">Payroll impact (required)</span></span>
- <span data-ttu-id="66c93-152">Susigrąžinti skolas</span><span class="sxs-lookup"><span data-stu-id="66c93-152">Recover arrears</span></span>
- <span data-ttu-id="66c93-153">Atskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="66c93-153">Deduction method</span></span>
- <span data-ttu-id="66c93-154">Atskaitymo pirmumas</span><span class="sxs-lookup"><span data-stu-id="66c93-154">Deduction priority</span></span>
- <span data-ttu-id="66c93-155">Apribojimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="66c93-155">Limit period</span></span>
- <span data-ttu-id="66c93-156">Limito suma</span><span class="sxs-lookup"><span data-stu-id="66c93-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="66c93-157">Išmokos</span><span class="sxs-lookup"><span data-stu-id="66c93-157">Benefits</span></span>

- <span data-ttu-id="66c93-158">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-158">Plan (required)</span></span>
- <span data-ttu-id="66c93-159">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-159">Type (required)</span></span>
- <span data-ttu-id="66c93-160">Parinktis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-160">Option (required)</span></span>
- <span data-ttu-id="66c93-161">Išmokos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-161">Benefit ID (required)</span></span>
- <span data-ttu-id="66c93-162">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="66c93-162">Frequency</span></span>
- <span data-ttu-id="66c93-163">Pagrindas</span><span class="sxs-lookup"><span data-stu-id="66c93-163">Basis</span></span>
- <span data-ttu-id="66c93-164">Suma arba tarifas</span><span class="sxs-lookup"><span data-stu-id="66c93-164">Amount or rate</span></span>
- <span data-ttu-id="66c93-165">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="66c93-166">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="66c93-166">Supported frequencies</span></span> 

- <span data-ttu-id="66c93-167">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="66c93-167">Weekly</span></span>
- <span data-ttu-id="66c93-168">Už dvi savaites</span><span class="sxs-lookup"><span data-stu-id="66c93-168">Bi-weekly</span></span>
- <span data-ttu-id="66c93-169">Kas pusę mėnesio</span><span class="sxs-lookup"><span data-stu-id="66c93-169">Semi-monthly</span></span>
- <span data-ttu-id="66c93-170">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="66c93-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="66c93-171">Palaikomos bazės</span><span class="sxs-lookup"><span data-stu-id="66c93-171">Supported bases</span></span> 

- <span data-ttu-id="66c93-172">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="66c93-172">Fixed amount</span></span>
- <span data-ttu-id="66c93-173">Pajamų procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="66c93-173">Percent of earnings</span></span>
- <span data-ttu-id="66c93-174">Produktyvios valandos</span><span class="sxs-lookup"><span data-stu-id="66c93-174">Productive hours</span></span>

<span data-ttu-id="66c93-175">„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.</span><span class="sxs-lookup"><span data-stu-id="66c93-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="66c93-176">Pasirinkimas „Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-176">Selection in Talent</span></span>        | <span data-ttu-id="66c93-177">Rezultatas „Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="66c93-178">None</span><span class="sxs-lookup"><span data-stu-id="66c93-178">None</span></span>                       | <span data-ttu-id="66c93-179">Nesukuriama jokio atskaitymo.</span><span class="sxs-lookup"><span data-stu-id="66c93-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="66c93-180">Tik atskaitymas</span><span class="sxs-lookup"><span data-stu-id="66c93-180">Deduction only</span></span>             | <span data-ttu-id="66c93-181">Sukuriamas darbuotojo atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="66c93-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="66c93-182">Tik įnašas</span><span class="sxs-lookup"><span data-stu-id="66c93-182">Contribution only</span></span>          | <span data-ttu-id="66c93-183">Sukuriamas darbdavio atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="66c93-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="66c93-184">Atskaitymas ir įnašas</span><span class="sxs-lookup"><span data-stu-id="66c93-184">Deduction and contribution</span></span> | <span data-ttu-id="66c93-185">Sukuriami darbuotojo ir darbdavio atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="66c93-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="66c93-186">Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="66c93-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="66c93-187">Pristatyti darbuotojų išmokų programą</span><span class="sxs-lookup"><span data-stu-id="66c93-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="66c93-188">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="66c93-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="66c93-189">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="66c93-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="66c93-190">Užregistruoti ir pašalinti išmokas darbuotojams</span><span class="sxs-lookup"><span data-stu-id="66c93-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="66c93-191">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="66c93-191">Compensation</span></span> 

<span data-ttu-id="66c93-192">Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="66c93-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="66c93-193">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="66c93-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="66c93-194">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="66c93-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="66c93-195">„Dayforce“ naudojama kompensacijos informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="66c93-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="66c93-196">Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="66c93-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="66c93-197">Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.</span><span class="sxs-lookup"><span data-stu-id="66c93-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="66c93-198">Daugiau informacijos apie kompensacijų planus rasite šios temose:</span><span class="sxs-lookup"><span data-stu-id="66c93-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="66c93-199">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="66c93-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="66c93-200">Kintamosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="66c93-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="66c93-201">Kurti atlyginimų / kompensavimo struktūrą ir planus</span><span class="sxs-lookup"><span data-stu-id="66c93-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="66c93-202">Kompensavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="66c93-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="66c93-203">Kompensavimo proceso nustatymas ir rezultatų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="66c93-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="66c93-204">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="66c93-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="66c93-205">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="66c93-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="66c93-206">Darbai</span><span class="sxs-lookup"><span data-stu-id="66c93-206">Jobs</span></span> 

<span data-ttu-id="66c93-207">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="66c93-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="66c93-208">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="66c93-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="66c93-209">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="66c93-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="66c93-210">Apibrėžti naujas užduotis</span><span class="sxs-lookup"><span data-stu-id="66c93-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="66c93-211">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="66c93-211">Positions</span></span>

<span data-ttu-id="66c93-212">Pareigos yra atskiros užduoties egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="66c93-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="66c93-213">Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="66c93-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="66c93-214">Pareigos egzistuoja padalinyje.</span><span class="sxs-lookup"><span data-stu-id="66c93-214">A position exists in a department.</span></span> <span data-ttu-id="66c93-215">Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="66c93-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="66c93-216">Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:</span><span class="sxs-lookup"><span data-stu-id="66c93-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="66c93-217">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-217">Position (required)</span></span>
- <span data-ttu-id="66c93-218">Aprašas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-218">Description (required)</span></span>
- <span data-ttu-id="66c93-219">Užduotis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-219">Job (required)</span></span>
- <span data-ttu-id="66c93-220">Padalinys (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-220">Department (required)</span></span>
- <span data-ttu-id="66c93-221">Pareigų tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-221">Position type (required)</span></span>
- <span data-ttu-id="66c93-222">Viso etato ekvivalentas</span><span class="sxs-lookup"><span data-stu-id="66c93-222">Full-time equivalent</span></span>
- <span data-ttu-id="66c93-223">Įprastos darbo valandos per metus (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="66c93-224">Apmokama juridinio subjekto (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="66c93-225">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-225">Pay cycle (required)</span></span>
- <span data-ttu-id="66c93-226">Numatytosios finansinės dimensijos – išlaidų centras (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="66c93-227">Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="66c93-228">Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.</span><span class="sxs-lookup"><span data-stu-id="66c93-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="66c93-229">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="66c93-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="66c93-230">Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas</span><span class="sxs-lookup"><span data-stu-id="66c93-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="66c93-231">Pareigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="66c93-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="66c93-232">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="66c93-232">Departments</span></span>

<span data-ttu-id="66c93-233">Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį.</span><span class="sxs-lookup"><span data-stu-id="66c93-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="66c93-234">Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą.</span><span class="sxs-lookup"><span data-stu-id="66c93-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="66c93-235">Padalinius galite naudoti norėdami pranešti apie funkcines sritis.</span><span class="sxs-lookup"><span data-stu-id="66c93-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="66c93-236">Padaliniai gali turėti pelno ir nuostolio atsakomybę.</span><span class="sxs-lookup"><span data-stu-id="66c93-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="66c93-237">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="66c93-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="66c93-238">Padalinio kūrimas ir priskyrimas padalinių hierarchijai</span><span class="sxs-lookup"><span data-stu-id="66c93-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="66c93-239">Apibrėžti naujus padalinius</span><span class="sxs-lookup"><span data-stu-id="66c93-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="66c93-240">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="66c93-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="66c93-241">Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams.</span><span class="sxs-lookup"><span data-stu-id="66c93-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="66c93-242">Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="66c93-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="66c93-243">Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="66c93-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="66c93-244">Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.</span><span class="sxs-lookup"><span data-stu-id="66c93-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="66c93-245">Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="66c93-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="66c93-246">Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="66c93-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="66c93-247">Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.</span><span class="sxs-lookup"><span data-stu-id="66c93-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="66c93-248">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="66c93-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="66c93-249">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-249">Pay cycle (required)</span></span>
- <span data-ttu-id="66c93-250">Mokėjimo ciklo dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="66c93-251">Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="66c93-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="66c93-252">Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="66c93-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="66c93-253">Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui.</span><span class="sxs-lookup"><span data-stu-id="66c93-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="66c93-254">Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="66c93-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="66c93-255">„Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Talent“.</span><span class="sxs-lookup"><span data-stu-id="66c93-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="66c93-256">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-256">Earning codes</span></span>

<span data-ttu-id="66c93-257">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="66c93-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="66c93-258">Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="66c93-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="66c93-259">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="66c93-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="66c93-260">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-260">Earning Code (required)</span></span>
- <span data-ttu-id="66c93-261">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-261">Description</span></span>
- <span data-ttu-id="66c93-262">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="66c93-262">Unit of measure</span></span>
- <span data-ttu-id="66c93-263">Produktyvus</span><span class="sxs-lookup"><span data-stu-id="66c93-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="66c93-264">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="66c93-264">Worker data</span></span>

<span data-ttu-id="66c93-265">Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms.</span><span class="sxs-lookup"><span data-stu-id="66c93-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="66c93-266">Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.</span><span class="sxs-lookup"><span data-stu-id="66c93-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="66c93-267">Galite tvarkyti šią darbininkų informaciją:</span><span class="sxs-lookup"><span data-stu-id="66c93-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="66c93-268">**Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.</span><span class="sxs-lookup"><span data-stu-id="66c93-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="66c93-269">**Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="66c93-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="66c93-270">**Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="66c93-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="66c93-271">**Kompensacija ir algalapis** – tvarkykite informaciją apie darbininko kompensacijos planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.</span><span class="sxs-lookup"><span data-stu-id="66c93-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="66c93-272">Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="66c93-273">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="66c93-273">General information</span></span>

- <span data-ttu-id="66c93-274">Darbuotojo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-274">Personnel number (required)</span></span>
- <span data-ttu-id="66c93-275">Vardas (būtinas)</span><span class="sxs-lookup"><span data-stu-id="66c93-275">First name (required)</span></span>
- <span data-ttu-id="66c93-276">Pavardė (būtinai)</span><span class="sxs-lookup"><span data-stu-id="66c93-276">Last name (required)</span></span>
- <span data-ttu-id="66c93-277">Antras vardas</span><span class="sxs-lookup"><span data-stu-id="66c93-277">Middle name</span></span>
- <span data-ttu-id="66c93-278">Paaukštinimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-278">Seniority date</span></span>
- <span data-ttu-id="66c93-279">Žinoma kaip</span><span class="sxs-lookup"><span data-stu-id="66c93-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="66c93-280">Asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="66c93-280">Personal information</span></span>

- <span data-ttu-id="66c93-281">Šeiminė padėtis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-281">Marital status (required)</span></span>
- <span data-ttu-id="66c93-282">Gimimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-282">Birth date (required)</span></span>
- <span data-ttu-id="66c93-283">Lytis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-283">Gender (required)</span></span>
- <span data-ttu-id="66c93-284">Asmuo su negalia</span><span class="sxs-lookup"><span data-stu-id="66c93-284">Person with disabilities</span></span>
- <span data-ttu-id="66c93-285">Pilietybės šalies regionas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="66c93-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="66c93-286">Adresas</span><span class="sxs-lookup"><span data-stu-id="66c93-286">Address information</span></span>

- <span data-ttu-id="66c93-287">Pagrindinis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-287">Primary (required)</span></span>
- <span data-ttu-id="66c93-288">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-288">Country/region (required)</span></span>
- <span data-ttu-id="66c93-289">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-289">Postal code (required)</span></span>
- <span data-ttu-id="66c93-290">Gatvės numeris (būtina) (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="66c93-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="66c93-291">Pastatų kompleksas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="66c93-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="66c93-292">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-292">City (required)</span></span>
- <span data-ttu-id="66c93-293">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-293">State (required)</span></span>
- <span data-ttu-id="66c93-294">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="66c93-295">Kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="66c93-295">Contact information</span></span> 

- <span data-ttu-id="66c93-296">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-296">Primary (required)</span></span>
- <span data-ttu-id="66c93-297">Kontakto numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-297">Contact number (required)</span></span>
- <span data-ttu-id="66c93-298">Išplėtimas</span><span class="sxs-lookup"><span data-stu-id="66c93-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="66c93-299">Algalapio informacija ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-299">Payroll information and earning codes</span></span>

<span data-ttu-id="66c93-300">Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="66c93-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="66c93-301">Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.</span><span class="sxs-lookup"><span data-stu-id="66c93-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="66c93-302">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-302">Earning codes</span></span>

- <span data-ttu-id="66c93-303">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-303">Position (required)</span></span>
- <span data-ttu-id="66c93-304">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-304">Earning Code (required)</span></span>
- <span data-ttu-id="66c93-305">Dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-305">Frequency (required)</span></span>
- <span data-ttu-id="66c93-306">Suma (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="66c93-307">Algalapių informacija</span><span class="sxs-lookup"><span data-stu-id="66c93-307">Payroll information</span></span>

- <span data-ttu-id="66c93-308">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="66c93-308">Payment Method</span></span>
- <span data-ttu-id="66c93-309">Ekonominė sritis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-309">Economic Region (required)</span></span>
- <span data-ttu-id="66c93-310">Darbuotojų išmokų ID</span><span class="sxs-lookup"><span data-stu-id="66c93-310">Employee Benefits ID</span></span>
- <span data-ttu-id="66c93-311">Asmens kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-311">National ID Number (required)</span></span>
- <span data-ttu-id="66c93-312">Karo tarnybos numeris</span><span class="sxs-lookup"><span data-stu-id="66c93-312">Military Service Number</span></span>
- <span data-ttu-id="66c93-313">Pamainos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-313">Shift ID (required)</span></span>
- <span data-ttu-id="66c93-314">Mokesčių numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-314">Tax Number (required)</span></span>
- <span data-ttu-id="66c93-315">Sąjungos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-315">Union ID (required)</span></span>
- <span data-ttu-id="66c93-316">Darbo dienos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-316">Work Day ID (required)</span></span>
- <span data-ttu-id="66c93-317">Darbo leidimo numeris</span><span class="sxs-lookup"><span data-stu-id="66c93-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="66c93-318">Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="66c93-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="66c93-319">Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.</span><span class="sxs-lookup"><span data-stu-id="66c93-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="66c93-320">Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="66c93-320">Employment details</span></span>

<span data-ttu-id="66c93-321">Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos.</span><span class="sxs-lookup"><span data-stu-id="66c93-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="66c93-322">„Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="66c93-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="66c93-323">Įdarbinimo pradžios data (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-323">Employment start date (required)</span></span>
- <span data-ttu-id="66c93-324">Įdarbinimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="66c93-324">Employment end date</span></span>
- <span data-ttu-id="66c93-325">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="66c93-325">Start date</span></span>
- <span data-ttu-id="66c93-326">Patikslinta darbo pradžios data</span><span class="sxs-lookup"><span data-stu-id="66c93-326">Adjusted start date</span></span>
- <span data-ttu-id="66c93-327">Atleidimo data (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="66c93-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="66c93-328">Atleidimo priežastis (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="66c93-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="66c93-329">Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="66c93-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="66c93-330">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-330">Talent</span></span>                | <span data-ttu-id="66c93-331">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c93-332">Naujausia samdos data</span><span class="sxs-lookup"><span data-stu-id="66c93-332">Most recent hire date</span></span> | <span data-ttu-id="66c93-333">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="66c93-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="66c93-334">Atleidimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-334">Termination date</span></span>      | <span data-ttu-id="66c93-335">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="66c93-336">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="66c93-336">Start date</span></span>            | <span data-ttu-id="66c93-337">Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="66c93-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="66c93-338">Pradinio įdarbinimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-338">Original hire date</span></span>    | <span data-ttu-id="66c93-339">Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="66c93-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="66c93-340">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="66c93-340">Compensation</span></span>

<span data-ttu-id="66c93-341">Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="66c93-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="66c93-342">Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="66c93-343">Įsigaliojimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-343">Effective Date (required)</span></span>
- <span data-ttu-id="66c93-344">Galiojimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="66c93-344">Expiration date</span></span>
- <span data-ttu-id="66c93-345">Užmokesčio tarifas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-345">Pay Rate (required)</span></span>
- <span data-ttu-id="66c93-346">Užmokesčio tarifo konvertavimas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="66c93-347">Metinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="66c93-348">Valandinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="66c93-349">Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="66c93-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="66c93-350">Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="66c93-351">Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="66c93-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="66c93-352">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="66c93-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="66c93-353">Socialinio draudimo identifikatorius</span><span class="sxs-lookup"><span data-stu-id="66c93-353">Social Security identifier</span></span> 

<span data-ttu-id="66c93-354">Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="66c93-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="66c93-355">Šis identifikatorius turi būti **SSN** identifikacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="66c93-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="66c93-356">„Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.</span><span class="sxs-lookup"><span data-stu-id="66c93-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="66c93-357">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-357">Primary (required)</span></span>
- <span data-ttu-id="66c93-358">Identifikacijos tipas = "SSN"</span><span class="sxs-lookup"><span data-stu-id="66c93-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="66c93-359">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-359">Issued Date</span></span>
- <span data-ttu-id="66c93-360">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-360">Expiration Date</span></span>

<span data-ttu-id="66c93-361">Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="66c93-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="66c93-362">Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.</span><span class="sxs-lookup"><span data-stu-id="66c93-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="66c93-363">Banko sąskaitos ir išmokos</span><span class="sxs-lookup"><span data-stu-id="66c93-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="66c93-364">Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="66c93-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="66c93-365">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-365">Talent</span></span>                         | <span data-ttu-id="66c93-366">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c93-367">Banko sąskaitos numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="66c93-368">SWIFT kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-368">SWIFT code (required)</span></span>          | <span data-ttu-id="66c93-369">**Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="66c93-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="66c93-370">Filialo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="66c93-371">Banko sąskaitos tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-371">Bank account type (required)</span></span>   | <span data-ttu-id="66c93-372">**Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="66c93-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="66c93-373">Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**.</span><span class="sxs-lookup"><span data-stu-id="66c93-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="66c93-374">Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke.</span><span class="sxs-lookup"><span data-stu-id="66c93-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="66c93-375">Visos kitos nelikutinės sąskaitos yra ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="66c93-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="66c93-376">Adresas</span><span class="sxs-lookup"><span data-stu-id="66c93-376">Address information</span></span>

<span data-ttu-id="66c93-377">Kiekvienas darbuotojas turi turėti vieną pirminę vietą.</span><span class="sxs-lookup"><span data-stu-id="66c93-377">Every employee must have one primary location.</span></span> <span data-ttu-id="66c93-378">„Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.</span><span class="sxs-lookup"><span data-stu-id="66c93-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="66c93-379">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-379">Primary (required)</span></span>
- <span data-ttu-id="66c93-380">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-380">Country/region (required)</span></span>
- <span data-ttu-id="66c93-381">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="66c93-382">Gatvė (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-382">Street (required)</span></span>
- <span data-ttu-id="66c93-383">Gatvės numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-383">Street Number (required)</span></span>
- <span data-ttu-id="66c93-384">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="66c93-384">Building Complement</span></span>
- <span data-ttu-id="66c93-385">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-385">City (required)</span></span>
- <span data-ttu-id="66c93-386">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-386">State (required)</span></span>
- <span data-ttu-id="66c93-387">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="66c93-388">Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje</span><span class="sxs-lookup"><span data-stu-id="66c93-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="66c93-389">Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="66c93-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="66c93-390">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="66c93-390">Departments are required on positions.</span></span>
- <span data-ttu-id="66c93-391">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="66c93-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="66c93-392">Galite sukonfigūruoti „Talent“, kad prie pareigų būtų nurodytas padalinys.</span><span class="sxs-lookup"><span data-stu-id="66c93-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="66c93-393">Norėdami tai atlikti, eikite į **Bendrinamos personalo pareigos > Pareigos > Prie pareigų reikalauti padalinių**.</span><span class="sxs-lookup"><span data-stu-id="66c93-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="66c93-394">Rekomenduojame integruojant šį parametrą taikyti.</span><span class="sxs-lookup"><span data-stu-id="66c93-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="66c93-395">Pareigų rūšys</span><span class="sxs-lookup"><span data-stu-id="66c93-395">Job types</span></span>

<span data-ttu-id="66c93-396">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="66c93-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="66c93-397">Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje.</span><span class="sxs-lookup"><span data-stu-id="66c93-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="66c93-398">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="66c93-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="66c93-399">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="66c93-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="66c93-400">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="66c93-401">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="66c93-401">Job type</span></span>   | <span data-ttu-id="66c93-402">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="66c93-403">Valandinis</span><span class="sxs-lookup"><span data-stu-id="66c93-403">Hourly</span></span>     | <span data-ttu-id="66c93-404">Valandinis</span><span class="sxs-lookup"><span data-stu-id="66c93-404">Hourly</span></span>      |
| <span data-ttu-id="66c93-405">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="66c93-405">Salaried</span></span>   | <span data-ttu-id="66c93-406">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="66c93-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="66c93-407">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="66c93-407">Position types</span></span> 

<span data-ttu-id="66c93-408">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="66c93-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="66c93-409">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="66c93-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="66c93-410">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="66c93-411">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="66c93-411">Position type</span></span>   | <span data-ttu-id="66c93-412">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="66c93-413">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-413">Full-time</span></span>       | <span data-ttu-id="66c93-414">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-414">Full time employee</span></span> |
| <span data-ttu-id="66c93-415">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-415">Part-time</span></span>       | <span data-ttu-id="66c93-416">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="66c93-417">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-417">Reason codes</span></span>

<span data-ttu-id="66c93-418">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="66c93-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="66c93-419">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="66c93-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="66c93-420">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="66c93-421">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="66c93-421">Reason code</span></span>    | <span data-ttu-id="66c93-422">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-422">Description</span></span>      | <span data-ttu-id="66c93-423">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="66c93-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="66c93-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="66c93-424">RESIGNATION</span></span>    | <span data-ttu-id="66c93-425">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="66c93-425">Resignation</span></span>      | <span data-ttu-id="66c93-426">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-426">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="66c93-427">TERMINATION</span></span>    | <span data-ttu-id="66c93-428">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="66c93-428">Termination</span></span>      | <span data-ttu-id="66c93-429">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-429">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="66c93-430">RETIREMENT</span></span>     | <span data-ttu-id="66c93-431">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="66c93-431">Retirement</span></span>       | <span data-ttu-id="66c93-432">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-432">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-433">KITA</span><span class="sxs-lookup"><span data-stu-id="66c93-433">OTHER</span></span>          | <span data-ttu-id="66c93-434">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="66c93-434">Other Reasons</span></span>    | <span data-ttu-id="66c93-435">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-435">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="66c93-436">DEATH</span></span>          | <span data-ttu-id="66c93-437">Mirtis</span><span class="sxs-lookup"><span data-stu-id="66c93-437">Death</span></span>            | <span data-ttu-id="66c93-438">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-438">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="66c93-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="66c93-440">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="66c93-440">Leave of Absence</span></span> | <span data-ttu-id="66c93-441">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-441">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="66c93-442">CONTRACTEND</span></span>    | <span data-ttu-id="66c93-443">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="66c93-443">End of Contract</span></span>  | <span data-ttu-id="66c93-444">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-444">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="66c93-445">SALARYCHANGE</span></span>   | <span data-ttu-id="66c93-446">Atlyginimo pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="66c93-446">Change of Salary</span></span> | <span data-ttu-id="66c93-447">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="66c93-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="66c93-448">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="66c93-448">Marital status</span></span>

<span data-ttu-id="66c93-449">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66c93-450">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="66c93-451">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-451">Talent</span></span>                 | <span data-ttu-id="66c93-452">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="66c93-453">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-453">Married</span></span>                | <span data-ttu-id="66c93-454">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-454">Married</span></span>              |
| <span data-ttu-id="66c93-455">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-455">Single</span></span>                 | <span data-ttu-id="66c93-456">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-456">Single</span></span>               |
| <span data-ttu-id="66c93-457">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="66c93-457">Widowed</span></span>                | <span data-ttu-id="66c93-458">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="66c93-458">Widowed</span></span>              |
| <span data-ttu-id="66c93-459">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="66c93-459">Divorced</span></span>               | <span data-ttu-id="66c93-460">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="66c93-460">Divorced</span></span>             |
| <span data-ttu-id="66c93-461">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="66c93-461">Registered Partnership</span></span> | <span data-ttu-id="66c93-462">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="66c93-462">Domestic Partnership</span></span> |
| <span data-ttu-id="66c93-463">None</span><span class="sxs-lookup"><span data-stu-id="66c93-463">None</span></span>                   | <span data-ttu-id="66c93-464">None</span><span class="sxs-lookup"><span data-stu-id="66c93-464">None</span></span>                 |
| <span data-ttu-id="66c93-465">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="66c93-465">Cohabiting</span></span>             | <span data-ttu-id="66c93-466">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="66c93-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="66c93-467">Giminė</span><span class="sxs-lookup"><span data-stu-id="66c93-467">Gender</span></span>

<span data-ttu-id="66c93-468">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66c93-469">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="66c93-470">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-470">Talent</span></span>       | <span data-ttu-id="66c93-471">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="66c93-472">Vyras</span><span class="sxs-lookup"><span data-stu-id="66c93-472">Male</span></span>         | <span data-ttu-id="66c93-473">Vyras</span><span class="sxs-lookup"><span data-stu-id="66c93-473">Male</span></span>            |
| <span data-ttu-id="66c93-474">Moteris</span><span class="sxs-lookup"><span data-stu-id="66c93-474">Female</span></span>       | <span data-ttu-id="66c93-475">Moteris</span><span class="sxs-lookup"><span data-stu-id="66c93-475">Female</span></span>          |
| <span data-ttu-id="66c93-476">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="66c93-476">Non-specific</span></span> | <span data-ttu-id="66c93-477">*Nepalaikoma*</span><span class="sxs-lookup"><span data-stu-id="66c93-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="66c93-478">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-478">Earning codes</span></span>

<span data-ttu-id="66c93-479">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="66c93-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="66c93-480">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="66c93-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="66c93-481">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="66c93-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="66c93-482">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="66c93-482">Supported frequencies</span></span>

- <span data-ttu-id="66c93-483">Visos</span><span class="sxs-lookup"><span data-stu-id="66c93-483">All</span></span>
- <span data-ttu-id="66c93-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="66c93-484">EVERYPAY</span></span>
- <span data-ttu-id="66c93-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="66c93-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="66c93-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="66c93-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="66c93-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="66c93-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="66c93-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-488">1OFMTH</span></span>
- <span data-ttu-id="66c93-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-489">LASTOFMTH</span></span>
- <span data-ttu-id="66c93-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-490">2OFMTH</span></span>
- <span data-ttu-id="66c93-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-491">3OFMTH</span></span>
- <span data-ttu-id="66c93-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-492">4OFMTH</span></span>
- <span data-ttu-id="66c93-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-493">5OFMTH</span></span>
- <span data-ttu-id="66c93-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-494">1N2OFMTH</span></span>
- <span data-ttu-id="66c93-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-495">3N4OFMTH</span></span>
- <span data-ttu-id="66c93-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-496">1N3OFMTH</span></span>
- <span data-ttu-id="66c93-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-497">1N4OFMTH</span></span>
- <span data-ttu-id="66c93-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-498">2N3OFMTH</span></span>
- <span data-ttu-id="66c93-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-499">2N4OFMTH</span></span>
- <span data-ttu-id="66c93-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="66c93-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="66c93-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="66c93-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="66c93-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="66c93-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="66c93-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="66c93-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="66c93-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="66c93-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="66c93-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="66c93-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="66c93-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="66c93-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="66c93-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="66c93-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66c93-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="66c93-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66c93-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="66c93-512">Adresai</span><span class="sxs-lookup"><span data-stu-id="66c93-512">Addresses</span></span>

<span data-ttu-id="66c93-513">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="66c93-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="66c93-514">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="66c93-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="66c93-515">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-515">Talent</span></span>          | <span data-ttu-id="66c93-516">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="66c93-517">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="66c93-517">Country/Region</span></span>  | <span data-ttu-id="66c93-518">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-518">Country Code</span></span>          |
| <span data-ttu-id="66c93-519">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-519">Zip/Postal Code</span></span> | <span data-ttu-id="66c93-520">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="66c93-520">Postal Code</span></span>           |
| <span data-ttu-id="66c93-521">Apskritis</span><span class="sxs-lookup"><span data-stu-id="66c93-521">State</span></span>           | <span data-ttu-id="66c93-522">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-522">State Code</span></span>            |
| <span data-ttu-id="66c93-523">Miestas</span><span class="sxs-lookup"><span data-stu-id="66c93-523">City</span></span>            | <span data-ttu-id="66c93-524">Miestas</span><span class="sxs-lookup"><span data-stu-id="66c93-524">City</span></span>                  |
| <span data-ttu-id="66c93-525">Apygarda</span><span class="sxs-lookup"><span data-stu-id="66c93-525">County</span></span>          | <span data-ttu-id="66c93-526">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="66c93-526">County (Municipality)</span></span> |
| <span data-ttu-id="66c93-527">Gatvė</span><span class="sxs-lookup"><span data-stu-id="66c93-527">Street</span></span>          | <span data-ttu-id="66c93-528">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="66c93-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="66c93-529">Mokesčių regionai</span><span class="sxs-lookup"><span data-stu-id="66c93-529">Tax regions</span></span>

<span data-ttu-id="66c93-530">Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį.</span><span class="sxs-lookup"><span data-stu-id="66c93-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="66c93-531">Mokesčių regionai yra susieti su „Dayforce“ vietų adresais.</span><span class="sxs-lookup"><span data-stu-id="66c93-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="66c93-532">Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis.</span><span class="sxs-lookup"><span data-stu-id="66c93-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="66c93-533">Mokesčių regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-533">Tax region (required)</span></span>
- <span data-ttu-id="66c93-534">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-534">Country/Region (required)</span></span>
- <span data-ttu-id="66c93-535">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-535">State (required)</span></span>
- <span data-ttu-id="66c93-536">Apygarda</span><span class="sxs-lookup"><span data-stu-id="66c93-536">County</span></span> 
- <span data-ttu-id="66c93-537">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="66c93-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="66c93-538">Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje</span><span class="sxs-lookup"><span data-stu-id="66c93-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="66c93-539">Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="66c93-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="66c93-540">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="66c93-540">Departments are required on positions.</span></span>
- <span data-ttu-id="66c93-541">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="66c93-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="66c93-542">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="66c93-542">Job types</span></span>

<span data-ttu-id="66c93-543">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="66c93-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="66c93-544">Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="66c93-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="66c93-545">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="66c93-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="66c93-546">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="66c93-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="66c93-547">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="66c93-548">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="66c93-548">Job type</span></span>   | <span data-ttu-id="66c93-549">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="66c93-550">Valandinis</span><span class="sxs-lookup"><span data-stu-id="66c93-550">Hourly</span></span>     | <span data-ttu-id="66c93-551">MX valandinis</span><span class="sxs-lookup"><span data-stu-id="66c93-551">MX Hourly</span></span>   |
| <span data-ttu-id="66c93-552">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="66c93-552">Salaried</span></span>   | <span data-ttu-id="66c93-553">MX fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="66c93-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="66c93-554">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="66c93-554">Position types</span></span> 

<span data-ttu-id="66c93-555">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="66c93-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="66c93-556">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="66c93-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="66c93-557">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="66c93-558">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="66c93-558">Position type</span></span>   | <span data-ttu-id="66c93-559">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="66c93-560">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-560">Full-time</span></span>       | <span data-ttu-id="66c93-561">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-561">Full time employee</span></span> |
| <span data-ttu-id="66c93-562">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-562">Part-time</span></span>       | <span data-ttu-id="66c93-563">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="66c93-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="66c93-564">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-564">Reason codes</span></span>

<span data-ttu-id="66c93-565">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="66c93-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="66c93-566">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="66c93-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="66c93-567">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="66c93-568">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="66c93-568">Reason code</span></span>            | <span data-ttu-id="66c93-569">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-569">Description</span></span>                    | <span data-ttu-id="66c93-570">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="66c93-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="66c93-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="66c93-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="66c93-572">Išvykimas prieš pirmą algalapį</span><span class="sxs-lookup"><span data-stu-id="66c93-572">Departure before first payroll</span></span> | <span data-ttu-id="66c93-573">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-573">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="66c93-574">RESIGNATION</span></span>            | <span data-ttu-id="66c93-575">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="66c93-575">Resignation</span></span>                    | <span data-ttu-id="66c93-576">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-576">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="66c93-577">PENSION</span></span>                | <span data-ttu-id="66c93-578">Pensija</span><span class="sxs-lookup"><span data-stu-id="66c93-578">Pension</span></span>                        | <span data-ttu-id="66c93-579">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-579">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="66c93-580">TERMINATION</span></span>            | <span data-ttu-id="66c93-581">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="66c93-581">Termination</span></span>                    | <span data-ttu-id="66c93-582">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-582">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="66c93-583">RETIREMENT</span></span>             | <span data-ttu-id="66c93-584">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="66c93-584">Retirement</span></span>                     | <span data-ttu-id="66c93-585">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-585">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="66c93-586">ABSENTEE</span></span>               | <span data-ttu-id="66c93-587">Nesantysis</span><span class="sxs-lookup"><span data-stu-id="66c93-587">Absentee</span></span>                       | <span data-ttu-id="66c93-588">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-588">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-589">KITA</span><span class="sxs-lookup"><span data-stu-id="66c93-589">OTHER</span></span>                  | <span data-ttu-id="66c93-590">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="66c93-590">Other Reasons</span></span>                  | <span data-ttu-id="66c93-591">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-591">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="66c93-592">CLOSURE</span></span>                | <span data-ttu-id="66c93-593">Įmonės uždarymas</span><span class="sxs-lookup"><span data-stu-id="66c93-593">Business Closure</span></span>               | <span data-ttu-id="66c93-594">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-594">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="66c93-595">DEATH</span></span>                  | <span data-ttu-id="66c93-596">Mirtis</span><span class="sxs-lookup"><span data-stu-id="66c93-596">Death</span></span>                          | <span data-ttu-id="66c93-597">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-597">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="66c93-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="66c93-599">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="66c93-599">Leave of Absence</span></span>               | <span data-ttu-id="66c93-600">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-600">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="66c93-601">CONTRACTEND</span></span>            | <span data-ttu-id="66c93-602">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="66c93-602">End of Contract</span></span>                | <span data-ttu-id="66c93-603">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="66c93-603">Terminate worker</span></span>     |
| <span data-ttu-id="66c93-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="66c93-604">SALARYCHANGE</span></span>           | <span data-ttu-id="66c93-605">Atlyginimo keitimas</span><span class="sxs-lookup"><span data-stu-id="66c93-605">Change of Salary</span></span>               | <span data-ttu-id="66c93-606">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="66c93-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="66c93-607">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="66c93-607">Terms of employment</span></span>

<span data-ttu-id="66c93-608">Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="66c93-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="66c93-609">Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.</span><span class="sxs-lookup"><span data-stu-id="66c93-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="66c93-610">Šios įdarbinimo sąlygos ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="66c93-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="66c93-611">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="66c93-611">Terms of employment</span></span>   | <span data-ttu-id="66c93-612">aprašymas</span><span class="sxs-lookup"><span data-stu-id="66c93-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="66c93-613">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="66c93-613">Regular</span></span>               | <span data-ttu-id="66c93-614">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="66c93-614">Regular</span></span>     |
| <span data-ttu-id="66c93-615">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="66c93-615">Direct</span></span>                | <span data-ttu-id="66c93-616">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="66c93-616">Direct</span></span>      |
| <span data-ttu-id="66c93-617">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="66c93-617">Internship</span></span>            | <span data-ttu-id="66c93-618">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="66c93-618">Internship</span></span>  |
| <span data-ttu-id="66c93-619">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="66c93-619">Permanent</span></span>             | <span data-ttu-id="66c93-620">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="66c93-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="66c93-621">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="66c93-621">Marital status</span></span>

<span data-ttu-id="66c93-622">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66c93-623">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="66c93-624">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-624">Talent</span></span>                 | <span data-ttu-id="66c93-625">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="66c93-626">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-626">Married</span></span>                | <span data-ttu-id="66c93-627">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-627">Married</span></span>                   |
| <span data-ttu-id="66c93-628">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-628">Single</span></span>                 | <span data-ttu-id="66c93-629">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="66c93-629">Single</span></span>                    |
| <span data-ttu-id="66c93-630">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="66c93-630">Widowed</span></span>                | <span data-ttu-id="66c93-631">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="66c93-631">Widowed</span></span>                   |
| <span data-ttu-id="66c93-632">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="66c93-632">Divorced</span></span>               | <span data-ttu-id="66c93-633">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="66c93-633">Divorced</span></span>                  |
| <span data-ttu-id="66c93-634">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="66c93-634">Registered Partnership</span></span> | <span data-ttu-id="66c93-635">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="66c93-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="66c93-636">None</span><span class="sxs-lookup"><span data-stu-id="66c93-636">None</span></span>                   | <span data-ttu-id="66c93-637">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66c93-638">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="66c93-638">Cohabiting</span></span>             | <span data-ttu-id="66c93-639">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="66c93-640">Giminė</span><span class="sxs-lookup"><span data-stu-id="66c93-640">Gender</span></span>

<span data-ttu-id="66c93-641">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66c93-642">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="66c93-643">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-643">Talent</span></span>       | <span data-ttu-id="66c93-644">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="66c93-645">Vyras</span><span class="sxs-lookup"><span data-stu-id="66c93-645">Male</span></span>         | <span data-ttu-id="66c93-646">Vyras</span><span class="sxs-lookup"><span data-stu-id="66c93-646">Male</span></span>                      |
| <span data-ttu-id="66c93-647">Moteris</span><span class="sxs-lookup"><span data-stu-id="66c93-647">Female</span></span>       | <span data-ttu-id="66c93-648">Moteris</span><span class="sxs-lookup"><span data-stu-id="66c93-648">Female</span></span>                    |
| <span data-ttu-id="66c93-649">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="66c93-649">Non-specific</span></span> | <span data-ttu-id="66c93-650">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="66c93-651">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="66c93-651">Payment method</span></span>

<span data-ttu-id="66c93-652">Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="66c93-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="66c93-653">Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66c93-654">Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="66c93-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="66c93-655">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-655">Talent</span></span>             | <span data-ttu-id="66c93-656">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="66c93-657">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="66c93-657">Cash</span></span>               | <span data-ttu-id="66c93-658">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="66c93-658">Cash</span></span>                      |
| <span data-ttu-id="66c93-659">Elektroninis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="66c93-659">Electronic Payment</span></span> | <span data-ttu-id="66c93-660">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="66c93-660">Transfer</span></span>                  |
| <span data-ttu-id="66c93-661">Tikrinti</span><span class="sxs-lookup"><span data-stu-id="66c93-661">Check</span></span>              | <span data-ttu-id="66c93-662">Čekis</span><span class="sxs-lookup"><span data-stu-id="66c93-662">Cheque</span></span>                    |
| <span data-ttu-id="66c93-663">Banko čekis</span><span class="sxs-lookup"><span data-stu-id="66c93-663">Bank Draft</span></span>         | <span data-ttu-id="66c93-664">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66c93-665">Kiti</span><span class="sxs-lookup"><span data-stu-id="66c93-665">Other</span></span>              | <span data-ttu-id="66c93-666">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="66c93-667">Banko sąskaitos tipas</span><span class="sxs-lookup"><span data-stu-id="66c93-667">Bank account type</span></span>

<span data-ttu-id="66c93-668">Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti.</span><span class="sxs-lookup"><span data-stu-id="66c93-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="66c93-669">Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="66c93-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="66c93-670">Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="66c93-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="66c93-671">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-671">Talent</span></span>            | <span data-ttu-id="66c93-672">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="66c93-673">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-673">Checking Account</span></span>  | <span data-ttu-id="66c93-674">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-674">CheckingAccount</span></span>           |
| <span data-ttu-id="66c93-675">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-675">Payroll Account</span></span>   | <span data-ttu-id="66c93-676">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-676">PayrollAccount</span></span>            |
| <span data-ttu-id="66c93-677">Taupomoji sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-677">Savings Account</span></span>   | <span data-ttu-id="66c93-678">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66c93-679">„BankGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-679">BankGirot account</span></span> | <span data-ttu-id="66c93-680">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66c93-681">„PlusGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="66c93-681">PlusGirot account</span></span> | <span data-ttu-id="66c93-682">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="66c93-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="66c93-683">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="66c93-683">Earning codes</span></span>

<span data-ttu-id="66c93-684">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="66c93-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="66c93-685">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="66c93-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="66c93-686">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="66c93-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="66c93-687">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="66c93-687">Supported frequencies</span></span>

- <span data-ttu-id="66c93-688">Visos</span><span class="sxs-lookup"><span data-stu-id="66c93-688">All</span></span>
- <span data-ttu-id="66c93-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="66c93-689">EVERYPAY</span></span>
- <span data-ttu-id="66c93-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="66c93-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="66c93-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="66c93-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="66c93-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="66c93-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="66c93-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-693">1OFMTH</span></span>
- <span data-ttu-id="66c93-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-694">LASTOFMTH</span></span>
- <span data-ttu-id="66c93-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-695">2OFMTH</span></span>
- <span data-ttu-id="66c93-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-696">3OFMTH</span></span>
- <span data-ttu-id="66c93-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-697">4OFMTH</span></span>
- <span data-ttu-id="66c93-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-698">5OFMTH</span></span>
- <span data-ttu-id="66c93-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-699">1N2OFMTH</span></span>
- <span data-ttu-id="66c93-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-700">3N4OFMTH</span></span>
- <span data-ttu-id="66c93-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-701">1N3OFMTH</span></span>
- <span data-ttu-id="66c93-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-702">1N4OFMTH</span></span>
- <span data-ttu-id="66c93-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-703">2N3OFMTH</span></span>
- <span data-ttu-id="66c93-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-704">2N4OFMTH</span></span>
- <span data-ttu-id="66c93-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="66c93-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="66c93-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="66c93-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="66c93-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66c93-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="66c93-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="66c93-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="66c93-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="66c93-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="66c93-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="66c93-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="66c93-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="66c93-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="66c93-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="66c93-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="66c93-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66c93-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="66c93-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66c93-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="66c93-717">Adresai</span><span class="sxs-lookup"><span data-stu-id="66c93-717">Addresses</span></span>

<span data-ttu-id="66c93-718">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="66c93-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="66c93-719">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="66c93-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="66c93-720">„Talent“</span><span class="sxs-lookup"><span data-stu-id="66c93-720">Talent</span></span>              | <span data-ttu-id="66c93-721">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="66c93-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="66c93-722">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="66c93-722">Country/Region</span></span>      | <span data-ttu-id="66c93-723">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-723">Country Code</span></span>          |
| <span data-ttu-id="66c93-724">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-724">Zip/Postal Code</span></span>     | <span data-ttu-id="66c93-725">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="66c93-725">Postal Code</span></span>           |
| <span data-ttu-id="66c93-726">Apskritis</span><span class="sxs-lookup"><span data-stu-id="66c93-726">State</span></span>               | <span data-ttu-id="66c93-727">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="66c93-727">State Code</span></span>            |
| <span data-ttu-id="66c93-728">Miestas</span><span class="sxs-lookup"><span data-stu-id="66c93-728">City</span></span>                | <span data-ttu-id="66c93-729">Miestas</span><span class="sxs-lookup"><span data-stu-id="66c93-729">City</span></span>                  |
| <span data-ttu-id="66c93-730">Apygarda</span><span class="sxs-lookup"><span data-stu-id="66c93-730">County</span></span>              | <span data-ttu-id="66c93-731">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="66c93-731">County (Municipality)</span></span> |
| <span data-ttu-id="66c93-732">Gatvė</span><span class="sxs-lookup"><span data-stu-id="66c93-732">Street</span></span>              | <span data-ttu-id="66c93-733">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="66c93-733">Address Line 1</span></span>        |
| <span data-ttu-id="66c93-734">Gatvė, namo nr.</span><span class="sxs-lookup"><span data-stu-id="66c93-734">Street Number</span></span>       | <span data-ttu-id="66c93-735">2 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="66c93-735">Address Line 2</span></span>        |
| <span data-ttu-id="66c93-736">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="66c93-736">Building Complement</span></span> | <span data-ttu-id="66c93-737">5 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="66c93-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="66c93-738">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="66c93-738">Passport number</span></span>

<span data-ttu-id="66c93-739">Darbuotojai gali paskelbti paso informaciją.</span><span class="sxs-lookup"><span data-stu-id="66c93-739">Employees can declare passport information.</span></span> <span data-ttu-id="66c93-740">Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.</span><span class="sxs-lookup"><span data-stu-id="66c93-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="66c93-741">Identifikacijos tipas = "Pasas"</span><span class="sxs-lookup"><span data-stu-id="66c93-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="66c93-742">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-742">Issued Date</span></span>
- <span data-ttu-id="66c93-743">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="66c93-743">Expiration Date</span></span>

<span data-ttu-id="66c93-744">Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="66c93-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="66c93-745">Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas.</span><span class="sxs-lookup"><span data-stu-id="66c93-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="66c93-746">Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.</span><span class="sxs-lookup"><span data-stu-id="66c93-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
