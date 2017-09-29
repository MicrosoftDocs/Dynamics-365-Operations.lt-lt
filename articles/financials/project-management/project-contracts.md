---
title: Projekto sutartys
description: "Šiame straipsnyje aprašomos projektų sutartys, kurias galite kurti įvairių tipų projektams ir lėšų skyrimo šaltiniams, aprašoma, kaip „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise‟ leidime galima valdyti sutartis ir projektų klientams išrašyti sąskaitas faktūras bei pateikiama viso to pavyzdžių."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2017

---

# <a name="project-contracts"></a><span data-ttu-id="a4af2-103">Projekto sutartys</span><span class="sxs-lookup"><span data-stu-id="a4af2-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a4af2-104">Šiame straipsnyje aprašomos projektų sutartys, kurias galite kurti įvairių tipų projektams ir lėšų skyrimo šaltiniams, aprašoma, kaip „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise‟ leidime galima valdyti sutartis ir projektų klientams išrašyti sąskaitas faktūras bei pateikiama viso to pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="a4af2-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="a4af2-105">Jūsų sukurtas projekto sutarties tipas nustato metodą, kuris naudojamas išrašyti SF projekto klientams.</span><span class="sxs-lookup"><span data-stu-id="a4af2-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="a4af2-106">Galite keisti projekto sutartį ir susijusį projektą, tačiau negalite keisti projekto tipo.</span><span class="sxs-lookup"><span data-stu-id="a4af2-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="a4af2-107">Naudodami projekto sutartį, vienu metu galite išrašyti vieno arba kelių projektų SF.</span><span class="sxs-lookup"><span data-stu-id="a4af2-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="a4af2-108">Projekto sutartis taip pat padeda užtikrinti nuoseklią SF išrašymo procedūrą kiekvienam projekto struktūros subprojektui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="a4af2-109">Kiekvienas projektas, kuriam bus išrašyta SF, turi būti susietas su projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="a4af2-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="a4af2-110">Projekto sutarties nuostatos taikomos visiems projektams ir subprojektams, susietiems su ta projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="a4af2-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="a4af2-111">Projekto sutartyje gali būti nurodytas vienas arba keli lėšų skyrimo šaltiniai.</span><span class="sxs-lookup"><span data-stu-id="a4af2-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="a4af2-112">Todėl galite išskaidyti sąskaitų pateikimą keliems finansuotojams, nustatyti lėšų limitus, kad iš lėšų skyrimo šaltinių nebūtų išskaityta didesnė nei nurodyta suma, ir konfigūruoti lėšų skyrimo taisykles, taikomas išlaidų padengimui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="a4af2-113">Projektų sutarčių finansavimas</span><span class="sxs-lookup"><span data-stu-id="a4af2-113">Funding for project contracts</span></span>
<span data-ttu-id="a4af2-114">Kai kuriose projektų sutartyse nurodyta, kad projekto išlaidų finansavimo atsakomybe dalijasi kelios šalys.</span><span class="sxs-lookup"><span data-stu-id="a4af2-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="a4af2-115">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="a4af2-115">Here are some examples:</span></span>

-   <span data-ttu-id="a4af2-116">Stambus klientas, turintis kelis padalinius, pageidauja, kad projekto finansavimas būtų išskaidytas pagal padalinį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="a4af2-117">Jūsų įmonė stambaus projekto išlaidomis dalijasi su išorės organizacija.</span><span class="sxs-lookup"><span data-stu-id="a4af2-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="a4af2-118">Kelių projektą kartu finansuoja dvi savivaldybės.</span><span class="sxs-lookup"><span data-stu-id="a4af2-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="a4af2-119">Tilto projektą finansuoja vyriausybės subsidija ir privati korporacija.</span><span class="sxs-lookup"><span data-stu-id="a4af2-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="a4af2-120">Sprendime „Finance and Operations‟ sąskaitą už vieną operaciją ar visą projektą galite išskaidyti keliems klientams, subsidijoms ar organizacijoms.</span><span class="sxs-lookup"><span data-stu-id="a4af2-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="a4af2-121">Projektuose, kuriuose yra keli finansuotojai, visos šalys, kurios prisideda prie išplėstinio finansavimo projekto, vadinamos finansavimo šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="a4af2-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="a4af2-122">Klientą, organizaciją ar subsidiją apibrėžus kaip finansavimo šaltinį, jį galima priskirti vienai ar kelioms finansavimo taisyklėms.</span><span class="sxs-lookup"><span data-stu-id="a4af2-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="a4af2-123">Finansavimo taisyklėse yra kriterijai, kurie nustato, kaip išlaidos paskirstomos įvairiems projekto finansavimo šaltiniams.</span><span class="sxs-lookup"><span data-stu-id="a4af2-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="a4af2-124">Kadangi atsargose laikomų prekių, pvz., rodomų pirkimo paraiškose ir pirkimo užsakymuose, išskaidyti negalima, platinant išlaidų sumos išskaidyti keliems finansavimo šaltiniams negalima.</span><span class="sxs-lookup"><span data-stu-id="a4af2-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="a4af2-125">Todėl, kol užregistruojamas atsargų išdavimas, finansavimo šaltinio reikšmė lieka 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="a4af2-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="a4af2-126">Užregistravus atsargų išdavimą, išlaidų suma paskirstoma atsižvelgiant į projekto sąskaitų paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="a4af2-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="a4af2-127">Toliau nurodyti keletas veiksmų, kuriuos galite atlikti, kad būtų lengviau sąskaitas išskaidyti keliems finansavimo šaltiniams.</span><span class="sxs-lookup"><span data-stu-id="a4af2-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="a4af2-128">Nurodykite, kad visose įvedamose projekto operacijose būtų naudojama ta pati pardavimo valiuta, kaip ir projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="a4af2-129">Nustatykite finansavimo limitus, kad finansavimo šaltiniui nebūtų išrašyta SF už didesnę nei nurodyta projekto sumą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="a4af2-130">Sukonfigūruokite kiekvieno darbuotojo, prekės, kategorijos, kategorijų grupės ir operacijos tipo (ar visų operacijų tipų) finansavimo taisykles ir finansavimo limitus.</span><span class="sxs-lookup"><span data-stu-id="a4af2-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="a4af2-131">Pasirinkite pasirinktines pradžios ir pabaigos datas, kad apibrėžtumėte laikotarpį, kada galioja kiekviena finansavimo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="a4af2-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="a4af2-132">Nurodykite procentą, už kurį atsakingas kiekvienas finansavimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="a4af2-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="a4af2-133">Nurodykite, kuris lėšų skyrimo šaltinis yra atsakingas už apvalinimo skirtumus, atsiradusius skaičiuojant finansavimo paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="a4af2-134">Nustatykite taisykles, nustatančias, kaip SF už projekto išlaidas išrašomos išoriniams klientams ir pateikiamos apmokėti vidinėms organizacijoms.</span><span class="sxs-lookup"><span data-stu-id="a4af2-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="a4af2-135">Operacijas įrašykite sulaikyto lėšų skyrimo sąskaitoje, kol bus galima gauti papildomų lėšų, arba kol nuspręsite apmokėti išlaidas viduje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="a4af2-136">Norint nustatyti, kurią mokesčių grupę susieti su operacija, projekte ieškoma mokesčių grupės priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="a4af2-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="a4af2-137">Jei projekto lygiu nepriskirta jokia mokesčių grupė, ieškoma projekto sutarties.</span><span class="sxs-lookup"><span data-stu-id="a4af2-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="a4af2-138">Pavyzdys: keli lėšų skyrimo šaltiniai (paprast.)</span><span class="sxs-lookup"><span data-stu-id="a4af2-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="a4af2-139">Toliau pateiktoje lentelėje pateikiami finansavimo paskirstymo keliems finansavimo šaltiniams valdymo scenarijai.</span><span class="sxs-lookup"><span data-stu-id="a4af2-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="a4af2-140">Šie scenarijai paremti toliau nurodytomis prielaidomis.</span><span class="sxs-lookup"><span data-stu-id="a4af2-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="a4af2-141">Prieš taikant kitus lėšų skyrimo taisyklių kriterijus, paskirstant lėšas įtraukiamos prioritetų nuostatos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="a4af2-142">Nenurodytas joks datų intervalas, todėl neapibrėžtas laikotarpis, kada lėšų skyrimo taisyklė galioja.</span><span class="sxs-lookup"><span data-stu-id="a4af2-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4af2-143"><strong>Scenarijus</strong></span><span class="sxs-lookup"><span data-stu-id="a4af2-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="a4af2-144"><strong>Lėšų skyrimo šaltinis </strong></span><span class="sxs-lookup"><span data-stu-id="a4af2-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="a4af2-145"><strong>Paskirstymo procentas </strong></span><span class="sxs-lookup"><span data-stu-id="a4af2-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="a4af2-146"><strong>Paskirstymo prioritetas </strong></span><span class="sxs-lookup"><span data-stu-id="a4af2-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4af2-147">Norite išlaidas paskirstyti vienam lėšų skyrimo šaltiniui, kol baigsis jo lėšos, išlaidas paskirstyti antram lėšų skyrimo šaltiniui, kol baigsi jo lėšos ir galiausiai likusias išlaidas paskirstyti trečiam lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-148">1　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4af2-149">2　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="a4af2-150">3　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-151">100 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-151">100%</span></span></li>
<li><span data-ttu-id="a4af2-152">100 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-152">100%</span></span></li>
<li><span data-ttu-id="a4af2-153">100 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-154">1</span><span class="sxs-lookup"><span data-stu-id="a4af2-154">1</span></span></li>
<li><span data-ttu-id="a4af2-155">2</span><span class="sxs-lookup"><span data-stu-id="a4af2-155">2</span></span></li>
<li><span data-ttu-id="a4af2-156">3</span><span class="sxs-lookup"><span data-stu-id="a4af2-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4af2-157">Norite 75 procentus išlaidų paskirstyti vienam lėšų skyrimo šaltiniui ir 25 procentus – antram lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="a4af2-158">Kai viename iš šių lėšų skyrimo šaltinių baigiasi lėšos, likusias išlaidas norite apmokėti iš trečio lėšų skyrimo šaltinio.</span><span class="sxs-lookup"><span data-stu-id="a4af2-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-159">1　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4af2-160">2　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="a4af2-161">3　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-162">75 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-162">75%</span></span></li>
<li><span data-ttu-id="a4af2-163">25 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-163">25%</span></span></li>
<li><span data-ttu-id="a4af2-164">100 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-165">1</span><span class="sxs-lookup"><span data-stu-id="a4af2-165">1</span></span></li>
<li><span data-ttu-id="a4af2-166">1</span><span class="sxs-lookup"><span data-stu-id="a4af2-166">1</span></span></li>
<li><span data-ttu-id="a4af2-167">2</span><span class="sxs-lookup"><span data-stu-id="a4af2-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4af2-168">Norite 75 procentus išlaidų paskirstyti vienam lėšų skyrimo šaltiniui ir 25 procentus – antram lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="a4af2-169">Kai viename iš šių lėšų skyrimo šaltinių baigiasi lėšos, likusias išlaidas norite išskaidyti trečiam lėšų skyrimo šaltiniui ir ketvirtam lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-170">1　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4af2-171">2　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="a4af2-172">3　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="a4af2-173">4　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-174">75 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-174">75%</span></span></li>
<li><span data-ttu-id="a4af2-175">25 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-175">25%</span></span></li>
<li><span data-ttu-id="a4af2-176">50 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-176">50%</span></span></li>
<li><span data-ttu-id="a4af2-177">50 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-178">1</span><span class="sxs-lookup"><span data-stu-id="a4af2-178">1</span></span></li>
<li><span data-ttu-id="a4af2-179">1</span><span class="sxs-lookup"><span data-stu-id="a4af2-179">1</span></span></li>
<li><span data-ttu-id="a4af2-180">2</span><span class="sxs-lookup"><span data-stu-id="a4af2-180">2</span></span></li>
<li><span data-ttu-id="a4af2-181">2</span><span class="sxs-lookup"><span data-stu-id="a4af2-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4af2-182">Norite pirmuosius 25 išlaidų procentus paskirstyti vienam lėšų skyrimo šaltiniui, o likusius – antram lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-183">1　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4af2-184">2　finansavimo　šaltinis</span><span class="sxs-lookup"><span data-stu-id="a4af2-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-185">25 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-185">25%</span></span></li>
<li><span data-ttu-id="a4af2-186">100 %</span><span class="sxs-lookup"><span data-stu-id="a4af2-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4af2-187">1</span><span class="sxs-lookup"><span data-stu-id="a4af2-187">1</span></span></li>
<li><span data-ttu-id="a4af2-188">2</span><span class="sxs-lookup"><span data-stu-id="a4af2-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="a4af2-189">Pavyzdys: keli lėšų skyrimo šaltiniai (sudėting.)</span><span class="sxs-lookup"><span data-stu-id="a4af2-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="a4af2-190">Turite tris lėšų skyrimo šaltinius, kuriuos norite naudoti toliau nurodyta tvarka.</span><span class="sxs-lookup"><span data-stu-id="a4af2-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="a4af2-191">2 lėšų skyrimo šaltinį ir 3 lėšų skyrimo šaltinį naudoti po lygiai, kol 2 lėšų skyrimo šaltinyje baigsis lėšos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="a4af2-192">Toliau naudoti 3 lėšų skyrimo šaltinį, kol jame baigsis lėšos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="a4af2-193">Kai 3 lėšų skyrimo šaltinyje baigiasi lėšos, naudoti 1 lėšų skyrimo šaltinį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="a4af2-194">Norėdami pasiekti šį tikslą, turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a4af2-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="a4af2-195">Atitinkamoms sumoms nustatykite 2 lėšų skyrimo šaltinio ir 3 lėšų skyrimo šaltinio lėšų limitus.</span><span class="sxs-lookup"><span data-stu-id="a4af2-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="a4af2-196">Sukurkite toliau nurodytas lėšų skyrimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="a4af2-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="a4af2-197">1 taisyklė (1 prioritetas): 50 procentų operacijų paskirstyti 2 lėšų skyrimo šaltiniui ir 50 procentų – 3 lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="a4af2-198">2 taisyklė (2 prioritetas): 100 procentų operacijų paskirstyti 3 lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="a4af2-199">3 taisyklė (3 prioritetas): 100 procentų operacijų paskirstyti 1 lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="a4af2-200">Ši sąranka veikia, nes operacijos tikrinamos pagal taisykles ir limitus, siekiant nustatyti, ar bet kuri (-is) iš jų taikoma (-as) operacijai.</span><span class="sxs-lookup"><span data-stu-id="a4af2-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="a4af2-201">Jei operacijai netaikomos jokios konkrečios taisyklės ar limitai, taikoma Visų operacijų taisyklė.</span><span class="sxs-lookup"><span data-stu-id="a4af2-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="a4af2-202">Visų operacijų taisyklė atitinka visas operacijas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="a4af2-203">Jei randama operaciją atitinkanti taisyklė, pirmiausia taikoma procentinė dalis, paskirstyta toje taisyklėje, bet tik atitikmenis patikrinus pagal visus nustatytus limitus.</span><span class="sxs-lookup"><span data-stu-id="a4af2-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="a4af2-204">Jei limitui atitikta, ir baigėsi lėšų skyrimo šaltinio lėšos, lėšų skyrimo taisyklės, susietos su lėšų limitu, nepaisoma, ir programa iėško kitos taikytinos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="a4af2-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="a4af2-205">Kai kuriais atvejais pagal taisyklę gali būti paskirstyta tik operacijos dalis.</span><span class="sxs-lookup"><span data-stu-id="a4af2-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="a4af2-206">Taip gali nutikti, nes, paskirstant operaciją, pasiekiamas limitas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="a4af2-207">Šiuo atveju pagal tą taisyklę paskirstoma tik tam tikra suma, pvz., 50 procentų kiekvienam lėšų skyrimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="a4af2-208">Taip taikoma 1 taisyklė, kuri aprašyta pirmiau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="a4af2-209">Likutis yra paskirstomas pagal kitą sekos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a4af2-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="a4af2-210">Toliau pateikiamoje lentelėje šis scenarijus nagrinėjamas išsamiau.</span><span class="sxs-lookup"><span data-stu-id="a4af2-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4af2-211"><strong>Dėmesio centras </strong></span><span class="sxs-lookup"><span data-stu-id="a4af2-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="a4af2-212"><strong>Informacija</strong></span><span class="sxs-lookup"><span data-stu-id="a4af2-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4af2-213">Lėšų skyrimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="a4af2-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-214">1 taisyklė (1 prioritetas): Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="a4af2-215">2 lėšų skyrimo šaltiniui paskirkite 50 proc. ir 3 lėšų skyrimo šaltiniui – 50 proc.</span><span class="sxs-lookup"><span data-stu-id="a4af2-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="a4af2-216">2 taisyklė (2 prioritetas): Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="a4af2-217">3 lėšų skyrimo šaltiniui paskirkite 100 proc.</span><span class="sxs-lookup"><span data-stu-id="a4af2-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="a4af2-218">3 taisyklė (2 prioritetas): Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="a4af2-219">1 lėšų skyrimo šaltiniui paskirkite 100 proc.</span><span class="sxs-lookup"><span data-stu-id="a4af2-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4af2-220">Lėšų limitai</span><span class="sxs-lookup"><span data-stu-id="a4af2-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-221">1 lėšų skyrimo šaltinio limitas = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="a4af2-222">2 lėšų skyrimo šaltinio limitas = 500,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="a4af2-223">3 lėšų skyrimo šaltinio limitas = 750,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4af2-224">1 operacija</span><span class="sxs-lookup"><span data-stu-id="a4af2-224">Transaction 1</span></span></td>
<td><span data-ttu-id="a4af2-225"><strong>Operacijos suma:</strong> 100,00<strong>Finansavimas:</strong> operacija apmokama tik pagal 1 taisyklę, nes, pritaikius 1 taisyklę, operacija yra visiškai apmokėta.</span><span class="sxs-lookup"><span data-stu-id="a4af2-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="a4af2-226">Operaciją po lygiai finansuoja 2 lėšų skyrimo šaltinis ir 3 lėšų skyrimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="a4af2-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="a4af2-227">2 lėšų skyrimo šaltinis: 50,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="a4af2-228">3 lėšų skyrimo šaltinis: 50,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4af2-229">2 operacija</span><span class="sxs-lookup"><span data-stu-id="a4af2-229">Transaction 2</span></span></td>
<td><span data-ttu-id="a4af2-230"><strong>Operacijos suma:</strong> 5 000,00<strong>Finansavimas:</strong> operacija apmokama pagal visas tris taisykles.<strong>1 taisyklė</strong>
</span><span class="sxs-lookup"><span data-stu-id="a4af2-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="a4af2-231">2 lėšų skyrimo šaltinis: 450,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="a4af2-232">3 lėšų skyrimo šaltinis: 450,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="a4af2-233">
<strong>2 taisyklė</strong>
</span><span class="sxs-lookup"><span data-stu-id="a4af2-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="a4af2-234">3 lėšų skyrimo šaltinis: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="a4af2-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="a4af2-235">
<strong>3 taisyklė</strong>
</span><span class="sxs-lookup"><span data-stu-id="a4af2-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="a4af2-236">1 lėšų skyrimo šaltinis: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="a4af2-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4af2-237">Visos lėšos, paskirstomos kiekvienam lėšų skyrimo šaltiniui</span><span class="sxs-lookup"><span data-stu-id="a4af2-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="a4af2-238">1 lėšų skyrimo šaltinis: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="a4af2-239">2 lėšų skyrimo šaltinis: 500,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="a4af2-240">3 lėšų skyrimo šaltinis: 750,00</span><span class="sxs-lookup"><span data-stu-id="a4af2-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="a4af2-241">Atsiskaitymo taisyklės</span><span class="sxs-lookup"><span data-stu-id="a4af2-241">Billing rules</span></span>
<span data-ttu-id="a4af2-242">Kai su klientu deratės dėl projekto sutarties, apibrėžiate, kaip ir kada galite išrašyti klientui SF už projekto darbą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="a4af2-243">Kai nustatote projekto sutartį ir projektą, galite nustatyti to projekto atsiskaitymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="a4af2-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="a4af2-244">Atsiskaitymo taisyklės yra pagrįstos projekto sąlygomis, kurios nurodytos projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="a4af2-245">Atsiskaitymo taisyklės, kurias galite sukurti, priklauso nuo projekto sutarties sąlygų ir projekto tipo, pavyzdžiui, laikas ir medžiaga arba fiksuota kaina, kurį susiejate su atsiskaitymo taisykle.</span><span class="sxs-lookup"><span data-stu-id="a4af2-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="a4af2-246">Galite sukurti daugiau nei vieną atsiskaitymo taisyklę projekto sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="a4af2-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="a4af2-247">Be to, atsiskaitymo taisyklę galite priskirti keliems projektams, susietiems su ta pačia projekto sutartimi ir kurių atsiskaitymo sąlygos yra panašios.</span><span class="sxs-lookup"><span data-stu-id="a4af2-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="a4af2-248">Galite nustatyti šiuos atsiskaitymo taisyklių tipus:</span><span class="sxs-lookup"><span data-stu-id="a4af2-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="a4af2-249">**Pristatymo vienetas** – klientui SF išrašyti baigus darbą su pristatymo vienetu.</span><span class="sxs-lookup"><span data-stu-id="a4af2-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="a4af2-250">Pristatymo vienetai apibrėžiami sutartyje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="a4af2-251">**Eiga** – klientui SF išrašyti įvykdžius nurodytą projekto procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="a4af2-252">Galite nustatyti atsiskaitymo taisyklę, kad automatiškai apskaičiuotų atlikto darbo procentinę dalį arba galite neautomatiškai apskaičiuoti atlikto darbo procentą ir klientui išrašytinos SF sumą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="a4af2-253">**Etapas** – SF klientui išrašyti už visą projekto etapo sumą, kai etapas pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="a4af2-254">**Mokestis** – klientui SF išrašyti už paslaugas ir įtraukti valdymo mokestį, kuris paprastai yra paslaugų savikainos procentas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="a4af2-255">**Laikas ir medžiagos** – klientui SF išrašyti už projekto laiką ir sunaudotas medžiagas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="a4af2-256">Visų tipų atsiskaitymo taisyklėse galite nurodyti užlaikymo procentinį dydį, kuris atskaitomas iš kliento SF, kol projektas pasiekia sutartą etapą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="a4af2-257">Mokėjimo užlaikymo procentas nurodomas projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="a4af2-258">Suma apskaičiuojama pagal bendrąją kliento SF eilučių vertę, ir iš jos atimama.</span><span class="sxs-lookup"><span data-stu-id="a4af2-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="a4af2-259">**Laiko ir medžiagų** bei **Eigos** atsiskaitymo taisykėms galite priskirti apmokestinimo kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="a4af2-260">Apmokestinimo kategorijos rodo operacijas, kurios turėtų būti įtrauktos į kliento SF.</span><span class="sxs-lookup"><span data-stu-id="a4af2-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="a4af2-261">Kai esate pasiruošę klientui išrašyti SF, projekto SF suma apskaičiuojama pagal atsiskaitymo taisykles ir sugeneruojamas projekto SF pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="a4af2-262">Tolesniuose skyriuose pateiktuose pavyzdžiuose parodyta, kaip nustatyti ir valdyti projekto atsiskaitymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="a4af2-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="a4af2-263">Pavyzdys: atsiskaitymo taisyklės kūrimas atsižvelgiant į pristatytų vienetų skaičių</span><span class="sxs-lookup"><span data-stu-id="a4af2-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="a4af2-264">Jūsų organizacija sutaria kliento darbuotojams suteikti iš viso penkias mokymo sesijas, kurių vienos kaina – 10 000.</span><span class="sxs-lookup"><span data-stu-id="a4af2-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="a4af2-265">SF klientui išrašote po kiekvienos mokymo sesijos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="a4af2-266">Nustatydami sutarties atsiskaitymo taisykles, naudojate toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="a4af2-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="a4af2-267">Pristatymo vienetas yra viena mokymo sesija.</span><span class="sxs-lookup"><span data-stu-id="a4af2-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="a4af2-268">Vieneto kaina yra 10 000 už mokymo sesiją.</span><span class="sxs-lookup"><span data-stu-id="a4af2-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="a4af2-269">Bendras vienetų skaičius yra penkios mokymo sesijos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="a4af2-270">Baigę vieną mokymo sesiją galite sukurti SF su 10 000 suma už pirmą pristatytą vienetą ir tą SF nusiųsti klientui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="a4af2-271">Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis nurodyta įvykdyta projekto procentine dalimi (apskaičiuota rankiniu būdu)</span><span class="sxs-lookup"><span data-stu-id="a4af2-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="a4af2-272">Jūsų organizacija, programinės įrangos konsultavimo įmonė, sudaro sutartį su klientu, kad sukurtų dalį kliento kuriamo produkto.</span><span class="sxs-lookup"><span data-stu-id="a4af2-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="a4af2-273">Jūsų organizacija sutinka per šešis mėnesius pateikti programinės įrangos kodą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="a4af2-274">Klientas sutinka sumokėti jūsų organizacijai už darbą iš viso 100 000.</span><span class="sxs-lookup"><span data-stu-id="a4af2-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="a4af2-275">Galite sukurti atsiskaitymo taisyklę norėdami išrašyti klientui SF pagal projekto atlikto darbo procentinę dalį, kaip nurodyta sutartyje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="a4af2-276">Pirmo mėnesio pabaigoje susitiksite su klientu norėdami nustatyti atlikto darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="a4af2-277">Jums ir klientui peržiūrėjus projektą, nusprendžiate, kad projekto įvykdyta 15 procentų.</span><span class="sxs-lookup"><span data-stu-id="a4af2-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="a4af2-278">Sukuriate SF 15 000 sumai (15 100 000 procentų) ir nusiunčiate ją klientui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="a4af2-279">Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis nurodyta įvykdyta projekto procentine dalimi (apskaičiuota automatiškai)</span><span class="sxs-lookup"><span data-stu-id="a4af2-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="a4af2-280">Jūsų organizacija, programinės įrangos kūrimo įmonė, sutinka klientui už 30 000 sukurti atlyginimų apskaitos paketą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="a4af2-281">Klientas sutinka mokėti jūsų organizacijai už atlikto darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="a4af2-282">Įvertinate, kad projekto išlaidos yra 20 000.</span><span class="sxs-lookup"><span data-stu-id="a4af2-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="a4af2-283">Projekto sutartyje nurodomos darbo kategorijos, naudotinos atsiskaitymo procese.</span><span class="sxs-lookup"><span data-stu-id="a4af2-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="a4af2-284">Galite nustatyti atsiskaitymo taisykles, kad SF sumos būtų automatiškai apskaičiuojamos pagal tai, kiek atlikta kiekvienos kategorijos darbų.</span><span class="sxs-lookup"><span data-stu-id="a4af2-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="a4af2-285">Nustatykite kiekvienos kategorijos biudžetą:</span><span class="sxs-lookup"><span data-stu-id="a4af2-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="a4af2-286">**Programavimas** – išlaidos – 15 000, įplaukos – 20 000</span><span class="sxs-lookup"><span data-stu-id="a4af2-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="a4af2-287">**Diegimas** – išlaidos – 5 000, įplaukos – 10 000</span><span class="sxs-lookup"><span data-stu-id="a4af2-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="a4af2-288">Pirmą kartą kuriant kliento SF, SF suma automatiškai apskaičiuojama remiantis tokia informacija:</span><span class="sxs-lookup"><span data-stu-id="a4af2-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="a4af2-289">Po mėnesio projekto darbuotojas pateikia projekto tabelį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="a4af2-290">Darbuotojo darbo valandų išlaidos yra 5 000 už programavimą ir 1 000 už diegimą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="a4af2-291">Atlikta 33 procentai programavimo darbo (5 000 faktinių išlaidų / 15 000 biudžeto išlaidų) ir 20 procentų diegimo darbo (1 000 faktinių išlaidų / 5 000 biudžeto išlaidų).</span><span class="sxs-lookup"><span data-stu-id="a4af2-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="a4af2-292">Automatiškai apskaičiuota SF suma: 8 667 (33 procentai nuo 20 000 + 20 procentų nuo 10 000).</span><span class="sxs-lookup"><span data-stu-id="a4af2-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="a4af2-293">Sukuriate SF 8 667 sumai ir nusiunčiate ją klientui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="a4af2-294">Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis sutartais etapais</span><span class="sxs-lookup"><span data-stu-id="a4af2-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="a4af2-295">Jūsų organizacija, valdymo konsultavimo įmonė, sutinka atlikti ketinamo parduoti kliento produkto rinkos tyrimą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="a4af2-296">Klientas sutinka tris mėnesius, pradedant nuo kovo mėnesio, naudotis jūsų paslaugomis ir sutinka jūsų organizacijai sumokėti 50 000.</span><span class="sxs-lookup"><span data-stu-id="a4af2-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="a4af2-297">Projektą sudaro trys etapai.</span><span class="sxs-lookup"><span data-stu-id="a4af2-297">The project has three milestones:</span></span>

-   <span data-ttu-id="a4af2-298">1 etapas: vartotojų duomenų rinkimas – kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4af2-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="a4af2-299">2 etapas: vartotojų duomenų analizė – balandžio 30 d.</span><span class="sxs-lookup"><span data-stu-id="a4af2-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="a4af2-300">3 etapas: produkto panaudojimo pasiūlymo pateikimas – gegužės 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4af2-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="a4af2-301">Klientas sutinka sumokėti jūsų organizacijai 10 000 už pirmąjį etapą, 20 000 už antrąjį etapą ir 20 000 už trečiąjį etapą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="a4af2-302">Kai sudarote projekto sutartį, sutinkate išrašyti klientui sąskaitą atsižvelgdami į atliktą etapą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="a4af2-303">Atsiskaitymo taisyklės nustatyme yra šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="a4af2-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="a4af2-304">Apibrėžkite projekto etapus.</span><span class="sxs-lookup"><span data-stu-id="a4af2-304">Define the project milestones.</span></span>
-   <span data-ttu-id="a4af2-305">Apibrėžkite sumą, kurią klientas turės sumokėti užbaigus kiekvieną etapą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="a4af2-306">Kai pirmasis etapas baigiamas kovo 31 d., jį pažymite kaip atliktą ir sukuriate SF su 10 000 suma bei ją nusiunčiate klientui.</span><span class="sxs-lookup"><span data-stu-id="a4af2-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="a4af2-307">Negalima sukurti etapo SF, kol etapas nepažymėtas kaip baigtas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="a4af2-308">Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis paslaugų ir valdymo mokesčiu</span><span class="sxs-lookup"><span data-stu-id="a4af2-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="a4af2-309">Jūsų organizacija, valdymo konsultavimo įmonė, sutinka vykdyti rinkos tyrimą ir įvertinti produkto, kurį klientas, mažmeninės prekybos įmonė, kuria, gyvybingumą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="a4af2-310">Sutarties sąlygose nurodyta, kad suteiksite savo trijų pagrindinių vadybos konsultantų paslaugas; jie atliks tyrimą atsižvelgdami į laiką ir medžiagas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="a4af2-311">Klientas sutinka už projekto konsultavimo valandą mokėti 100 ir 10 procentų valdymo mokestį.</span><span class="sxs-lookup"><span data-stu-id="a4af2-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="a4af2-312">Kai sudarote projekto sutartį, sukurkite atsiskaitymo taisyklę norėdami 10 procentų valdymo mokestį pridėti prie apmokamų projekto konsultavimo valandų.</span><span class="sxs-lookup"><span data-stu-id="a4af2-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="a4af2-313">Kuriant kliento SF, įtraukiamas 10 procentų valdymo mokestis ir konsultavimo valandų išlaidos.</span><span class="sxs-lookup"><span data-stu-id="a4af2-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="a4af2-314">Pavyzdžiui, jei trys konsultantai iš viso projektui skyrė 200 valandų, pagal toliau nurodytą skaičiavimą sukuriama SF su 22 000 suma.</span><span class="sxs-lookup"><span data-stu-id="a4af2-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="a4af2-315">200 valandų, 100 už valandą = 20 000</span><span class="sxs-lookup"><span data-stu-id="a4af2-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="a4af2-316">10 procentų valdymo mokestis = 2 000</span><span class="sxs-lookup"><span data-stu-id="a4af2-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="a4af2-317">Bendroji SF suma = 22 000</span><span class="sxs-lookup"><span data-stu-id="a4af2-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="a4af2-318">Jei mokesčius moka klientas ir projekto sutartyje pasirenkate PVM grupę, PVM grupė automatiškai įvedama į mokesčių atsiskaitymo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a4af2-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="a4af2-319">Pavyzdys: atsiskaitymo taisyklės kūrimas atsižvelgiant į laiko ir medžiagų vertę</span><span class="sxs-lookup"><span data-stu-id="a4af2-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="a4af2-320">Jūsų organizacija, programinės įrangos konsultavimo įmonė, sutinka pateikti penkis techninius konsultantus dirbti programinės įrangos kūrimo projekte klientui per ateinančius šešis mėnesius.</span><span class="sxs-lookup"><span data-stu-id="a4af2-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="a4af2-321">Klientas sutinka mokėti 150 už kiekvieną konsultavimo valandą ir padengti biuro reikmenų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="a4af2-322">Jūsų organizacija siųs klientui SF kiekvieno mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="a4af2-323">Kai sudarote projekto sutartį, sutinkate kas mėnesį išrašyti klientui sąskaitą atsižvelgdami projekto į laiką ir medžiagas.</span><span class="sxs-lookup"><span data-stu-id="a4af2-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="a4af2-324">Sukurkite atsiskaitymo taisyklę su šia informacija:</span><span class="sxs-lookup"><span data-stu-id="a4af2-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="a4af2-325">Sutarties laikotarpis yra šeši mėnesiai.</span><span class="sxs-lookup"><span data-stu-id="a4af2-325">The contract period is six months.</span></span>
-   <span data-ttu-id="a4af2-326">Konsultavimo laikas apskaičiuojamas už valandą taikant 150 tarifą.</span><span class="sxs-lookup"><span data-stu-id="a4af2-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="a4af2-327">Biuro reikmenims SF išrašoma su tam tikra suma, o visos projekto išlaidos neturi viršyti 10 000.</span><span class="sxs-lookup"><span data-stu-id="a4af2-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="a4af2-328">Vykdydami projektą sukurkite kliento SF kiekvieno kalendorinio mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="a4af2-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="a4af2-329">Pirmąjį mėnesį projekto konsultantai iš viso įrašė 800 valandų.</span><span class="sxs-lookup"><span data-stu-id="a4af2-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="a4af2-330">Projekto biuro reikmenų išlaidos yra 2 000.</span><span class="sxs-lookup"><span data-stu-id="a4af2-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="a4af2-331">Todėl mėnesio pabaigoje sukurkite SF su 122 000 suma: 800 valandų po 150 už valandą ir 2 000 už biuro reikmenis.</span><span class="sxs-lookup"><span data-stu-id="a4af2-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



