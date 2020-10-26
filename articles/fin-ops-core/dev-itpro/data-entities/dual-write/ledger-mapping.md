---
title: Integruota didžioji knyga
description: Šioje temoje aprašomas didžiosios knygos duomenų integravimas tarp „Finance and Operations“ ir kitų „Dynamics 365“ programų, naudojant „Common Data Service“.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 20c038d0d4fe8ec3e07219862f98aef970882f26
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985250"
---
# <a name="integrated-ledger"></a><span data-ttu-id="48d2f-103">Integruota didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="48d2f-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="48d2f-104">Verslo programoje didžiosios knygos duomenimis nustatoma pagrindinė sąranka, kaip įmonė vykdo veiklą.</span><span class="sxs-lookup"><span data-stu-id="48d2f-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="48d2f-105">Pavyzdžiui, didžiosios knygos duomenimis nurodomi finansiniai metai, kurių įmonė laikosi, valiutos, kuriomis ji atlieka operacijas, ir naudojamos sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="48d2f-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="48d2f-106">Šioje temoje aprašomas šių pagrindinių finansinių duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="48d2f-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="48d2f-107">Šablonai</span><span class="sxs-lookup"><span data-stu-id="48d2f-107">Templates</span></span>

<span data-ttu-id="48d2f-108">Didžiosios knygos duomenis sudaro pagrindinių finansinių objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="48d2f-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="48d2f-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="48d2f-109">Finance and Operations apps</span></span>      | <span data-ttu-id="48d2f-110">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="48d2f-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="48d2f-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="48d2f-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="48d2f-112">Valiutos</span><span class="sxs-lookup"><span data-stu-id="48d2f-112">Currencies</span></span>                       | <span data-ttu-id="48d2f-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="48d2f-113">transactioncurrencies</span></span>            |
<span data-ttu-id="48d2f-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="48d2f-114">FiscalCalendar</span></span>                   | <span data-ttu-id="48d2f-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="48d2f-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="48d2f-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="48d2f-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="48d2f-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="48d2f-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="48d2f-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="48d2f-118">ExchRateType</span></span>                     | <span data-ttu-id="48d2f-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="48d2f-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="48d2f-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="48d2f-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="48d2f-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="48d2f-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="48d2f-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="48d2f-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="48d2f-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="48d2f-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="48d2f-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="48d2f-124">MainAccountCategory</span></span>              | <span data-ttu-id="48d2f-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="48d2f-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="48d2f-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="48d2f-126">MainAccount</span></span>                      | <span data-ttu-id="48d2f-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="48d2f-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="48d2f-128">DK</span><span class="sxs-lookup"><span data-stu-id="48d2f-128">Ledger</span></span>                           | <span data-ttu-id="48d2f-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="48d2f-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="48d2f-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="48d2f-130">ExchangeRates</span></span>                    | <span data-ttu-id="48d2f-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="48d2f-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="48d2f-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="48d2f-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="48d2f-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="48d2f-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="48d2f-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="48d2f-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="48d2f-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="48d2f-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="48d2f-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="48d2f-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="48d2f-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="48d2f-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="48d2f-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="48d2f-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="48d2f-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="48d2f-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




