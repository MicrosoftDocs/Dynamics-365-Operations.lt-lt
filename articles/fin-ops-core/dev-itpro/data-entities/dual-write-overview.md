---
title: Beveik realiuoju laiku vykstantis duomenų integravimas su „Common Data Service”
description: Šioje temoje apžvelgiamas integravimas tarp „Finance and Operations“ programų ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853911"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="33a42-103">Beveik realiuoju laiku vykstantis duomenų integravimas su „Common Data Service”</span><span class="sxs-lookup"><span data-stu-id="33a42-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33a42-104">Šiame skaitmeniniame pasaulyje verslo ekosistemos naudoja „Microsoft Dynamics 365“ programas kaip visumą.</span><span class="sxs-lookup"><span data-stu-id="33a42-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="33a42-105">Kadangi žmonių, klientų, operacijų ir daiktų interneto („IoT“) įrenginiai patenka į vieną šaltinį, galimos skaitmeninės grįžtamojo ryšio spragos.</span><span class="sxs-lookup"><span data-stu-id="33a42-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="33a42-106">Norint pasiekti šią patirtį, būtinas integravimas tarp „Finance and Operations“ ir „Dynamics 365“ programų.</span><span class="sxs-lookup"><span data-stu-id="33a42-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="33a42-107">Kai kurios programos sukurtos remiantis „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="33a42-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="33a42-108">„Finance and Operations“ programų duomenų integravimas su „Common Data Service“ leidžia kitoms programoms nuosekliai ir sklandžiai sąveikauti su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="33a42-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="33a42-109">„Finance and Operations“ programos ir „Common Data Service“ pateikia beveik realaus laiko duomenų sinchronizavimą tarp „Finance and Operations“ programų ir kitų „Dynamics 365” programų per dvigubo rašymo sistemą.</span><span class="sxs-lookup"><span data-stu-id="33a42-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="33a42-110">Padengimas yra platus ir apima 28 programos paviršiaus sritis.</span><span class="sxs-lookup"><span data-stu-id="33a42-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="33a42-111">Tikslas yra suteikti „One Dynamics 365“ vartotojo patirtį per sklandžius duomenų srautus, kurie jungia verslo procesus visose programose.</span><span class="sxs-lookup"><span data-stu-id="33a42-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Struktūros apžvalgos diagrama](media/dual-write-overview.jpg)

<span data-ttu-id="33a42-113">Galimi tolesni vertės pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="33a42-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="33a42-114">Organizacijos hierarchija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="33a42-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="33a42-115">Įmonės sąvoka programoje „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="33a42-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="33a42-116">Integruotas kliento šablonas</span><span class="sxs-lookup"><span data-stu-id="33a42-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="33a42-117">Integruota didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="33a42-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="33a42-118">Bendrosios produkto funkcijos</span><span class="sxs-lookup"><span data-stu-id="33a42-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="33a42-119">Integruotas tiekėjo šablonas</span><span class="sxs-lookup"><span data-stu-id="33a42-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="33a42-120">Integruotos svetainės ir sandėliai</span><span class="sxs-lookup"><span data-stu-id="33a42-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="33a42-121">Bendrieji integruotų mokesčių duomenys</span><span class="sxs-lookup"><span data-stu-id="33a42-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="33a42-122">Sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="33a42-122">System requirements</span></span>

<span data-ttu-id="33a42-123">Sinchroninis, dvikryptis, beveik realiojo laiko duomenų srautams reikia šių versijų:</span><span class="sxs-lookup"><span data-stu-id="33a42-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="33a42-124">Microsoft Dynamics 365 for Finance and Operations 10.0.4 versija (2019 m. liepos mėn.) su 28 arba naujesniu platformos versija</span><span class="sxs-lookup"><span data-stu-id="33a42-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="33a42-125">Microsoft Dynamics 365 for Customer Engagement, 9.1 (4.2) arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="33a42-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="33a42-126">Sąrankos instrukcijos</span><span class="sxs-lookup"><span data-stu-id="33a42-126">Setup instructions</span></span>

<span data-ttu-id="33a42-127">Atlikite šiuos veiksmus, kad nustatytumėte „Finance and Operations“ programų ir „Common Data Service“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="33a42-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="33a42-128">Informacijos apie dvigubo rašymo sistemos diegimą ieškokite [išsamiame vadove](https://aka.ms/dualwrite-docs) temoje „Dbigubo rašymo peržiūros paskelbimas“.</span><span class="sxs-lookup"><span data-stu-id="33a42-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="33a42-129">Sprendimą atsisiųskite ir įdiekite iš „Yammer“ grupės [„Fin Ops and CDS/CE Integration via Dual-Write“](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096).</span><span class="sxs-lookup"><span data-stu-id="33a42-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="33a42-130">Pakete yra penki sprendimai:</span><span class="sxs-lookup"><span data-stu-id="33a42-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="33a42-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="33a42-131">Dynamics365Company</span></span>
    + <span data-ttu-id="33a42-132">Valiutų kursai</span><span class="sxs-lookup"><span data-stu-id="33a42-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="33a42-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="33a42-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="33a42-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="33a42-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="33a42-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="33a42-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="33a42-136">Sekite vykdymo tvarką, skirtą [pradinių nuorodos duomenų sinchronizavimui](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="33a42-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="33a42-137">Jei susiduriate su dvigubo rašymo sinchronizavimo problemomis, žr. [„Duomenų integravimo tirikčių šalinimo vadovas](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="33a42-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33a42-138">Jūs negalite vienu metu paleisti funkcijos [Potencialus klientas į grynuosius pinigus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) ir dvigubo rašymo.</span><span class="sxs-lookup"><span data-stu-id="33a42-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="33a42-139">Jei naudojate potencialaus kliento į grynuosius pinigus sprendimą, turite jį pašalinti.</span><span class="sxs-lookup"><span data-stu-id="33a42-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="33a42-140">Taip pat turite išjungti kliento ir tiekėjo dvigubo rašymo šablonus, kurie yra potencialaus kliento į grynuosius pinigus sprendimo dalis.</span><span class="sxs-lookup"><span data-stu-id="33a42-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
