---
title: Mažmeninės prekybos operacijų vientisumo tikrintuvas
description: Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos „Microsoft Dynamics 365 for Retail“.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 8b373ce3cfd1183a082e2b1ebaf8c907b16e581e
ms.sourcegitcommit: ca4562fafa33b3512f0a5e246b15545fcf53e834
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2019
ms.locfileid: "379998"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="d5ad6-103">Mažmeninės prekybos operacijų vientisumo tikrintuvas</span><span class="sxs-lookup"><span data-stu-id="d5ad6-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="d5ad6-104">Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos, veikiančios „Microsoft Dynamics 365 for Finance and Operations“ 8.1.3 versijoje.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="d5ad6-105">Vientisumo tikrintuvas identifikuoja ir atskiria nesuderinamas operacijas prieš jas paimant į išrašų registravimo procesą.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="d5ad6-106">Išrašą registruojant „Retail“, užregistruoti gali nepavykti dėl mažmeninės prekybos operacijų lentelėse esančių nesuderinamų duomenų.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="d5ad6-107">Duomenų problema galėjo įvykti dėl nenumatytų problemų elektroninio kasos aparato (EKA) programoje arba dėl netinkamo operacijų importavimo iš trečiųjų šalių EKA sistemų.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="d5ad6-108">Šio nesuderinamumo atvejų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="d5ad6-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="d5ad6-109">Operacijų suma, nurodyta antraštės lentelėje, nesutampa su eilučių operacijų suma.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="d5ad6-110">Eilučių skaičius, nurodytas antraštės lentelėje, nesutampa su operacijų lentelės eilučių skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="d5ad6-111">Mokesčiai, nurodyti antraštės lentelėje, nesutampa su mokesčių suma eilutėse.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="d5ad6-112">Kai nesuderinamos operacijos paimamos į išrašo registravimo procesą, sukuriamos nesuderinamos pardavimo SF ir mokėjimo žurnalai, todėl nepavyksta visas išrašų registravimo procesas.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="d5ad6-113">Norint atkurti išrašus iš tokios būsenos reikia pataisyti nemažai duomenų įvairiose operacijų lentelėse.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="d5ad6-114">Mažmeninės prekybos operacijų vientisumo tikrintuvas apsaugo nuo tokių problemų.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="d5ad6-115">Šioje diagramoje parodytas registravimo procesas naudojant operacijų vientisumo tikrintuvą.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="d5ad6-116">![Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą](./media/validchecker.png "Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą")</span><span class="sxs-lookup"><span data-stu-id="d5ad6-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="d5ad6-117">Paketinis vykdymas **Tikrinti parduotuvės operacijas** tikrina mažmeninės prekybos operacijų lentelių vientisumą tolesniais aspektais.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="d5ad6-118">Kliento kodas – tikrinama, ar kliento kodas, nurodytas mažmeninės prekybos operacijų lentelėse, yra HQ kliento bendruosiuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="d5ad6-119">Eilučių skaičius – tikrinama, ar eilučių skaičius, nurodytas operacijos antraštės lentelėje, sutampa su pardavimo operacijų lentelių eilučių skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="d5ad6-120">Vientisumo tikrintuvo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d5ad6-120">Set up the consistency checker</span></span>
<span data-ttu-id="d5ad6-121">Sukonfigūruokite, kad paketinis vykdymas Tikrinti parduotuvės operacijas būtų paleidžiamas periodiškai, įėję į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> EKA registravimas**.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="d5ad6-122">Paketinė užduotis gali būtu suplanuota pagal parduotuvės organizacijos hierarchiją, panašiai kaip nustatyti procesai Skaičiuoti išrašus pakete ir Registruoti išrašus pakete.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="d5ad6-123">Rekomenduojame sukonfigūruoti šį paketinį vykdymą, kad jis būtų paleistas keletą kartų per dieną, ir suplanuoti taip, kad jis būtų vykdomas kiekvienos P užduoties pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="d5ad6-124">Tikrinimo proceso rezultatai</span><span class="sxs-lookup"><span data-stu-id="d5ad6-124">Results of validation process</span></span>
<span data-ttu-id="d5ad6-125">Paketinio vykdymo tikrinimo rezultatai yra pažymimi atitinkamoje mažmeninės prekybos operacijoje.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="d5ad6-126">Mažmeninės prekybos operacijos įrašo lauko **Tikrinimo būsena** reikšmė pateikiama arba **Sėkmingai**, arba **Klaida**, o lauke **Paskutinio tikrinimo laikas** rodoma paskutinio tikrinimo data.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="d5ad6-127">Norėdami peržiūrėti išsamesnį klaidos tekstą tikrinimui nepavykus, pasirinkite atitinkamą mažmeninės prekybos parduotuvės operacijos įrašą ir spustelėkite mygtuką **Tikrinimo klaidos**.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="d5ad6-128">Operacijos, kurias tikrinant rasta klaidų ir kurios dar nebuvo patikrintos, į išrašus įtrauktos nebus.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="d5ad6-129">Proceso Skaičiuoti išrašą metu vartotojams bus pranešta, jei bus operacijų, kurios galėjo būti įtrauktos į išrašą, tačiau nebuvo.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="d5ad6-130">Radus tikrinimo klaidų, vienintelis būdas jas ištaisyti yra kreiptis į „Microsoft“ pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="d5ad6-131">Būsimame leidime bus įtraukta galimybė vartotojui pataisyti klaidingus įrašus vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="d5ad6-132">Be to, pradės veikti registravimo ir audito funkcijos, kad būtų galima sekti pakeitimų retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="d5ad6-133">Į būsimas versijas bus įtraukta papildomų tikrinimo taisyklių, kurios palaikys daugiau scenarijų.</span><span class="sxs-lookup"><span data-stu-id="d5ad6-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
