---
title: Integruota didžioji knyga
description: Šioje temoje aprašomas didžiosios knygos duomenų integravimas tarp „Finance and Operations“ ir kitų „Dynamics 365“ programų, naudojant „Dataverse“.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5fedcbcd8db2692214ea66b2fbab9f7381e0a622
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748522"
---
# <a name="integrated-ledger"></a><span data-ttu-id="d1581-103">Integruota didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="d1581-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="d1581-104">Verslo programoje didžiosios knygos duomenimis nustatoma pagrindinė sąranka, kaip įmonė vykdo veiklą.</span><span class="sxs-lookup"><span data-stu-id="d1581-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="d1581-105">Pavyzdžiui, didžiosios knygos duomenimis nurodomi finansiniai metai, kurių įmonė laikosi, valiutos, kuriomis ji atlieka operacijas, ir naudojamos sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="d1581-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="d1581-106">Šioje temoje aprašomas šių pagrindinių finansinių duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="d1581-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="d1581-107">Šablonai</span><span class="sxs-lookup"><span data-stu-id="d1581-107">Templates</span></span>

<span data-ttu-id="d1581-108">Didžiosios knygos duomenis sudaro pagrindinių finansinių lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="d1581-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="d1581-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="d1581-109">Finance and Operations apps</span></span>      | <span data-ttu-id="d1581-110">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="d1581-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="d1581-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d1581-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="d1581-112">Valiutos</span><span class="sxs-lookup"><span data-stu-id="d1581-112">Currencies</span></span>                       | <span data-ttu-id="d1581-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="d1581-113">transactioncurrencies</span></span>            |
<span data-ttu-id="d1581-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="d1581-114">FiscalCalendar</span></span>                   | <span data-ttu-id="d1581-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="d1581-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="d1581-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="d1581-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="d1581-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="d1581-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="d1581-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="d1581-118">ExchRateType</span></span>                     | <span data-ttu-id="d1581-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="d1581-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="d1581-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="d1581-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="d1581-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="d1581-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="d1581-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="d1581-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="d1581-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="d1581-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="d1581-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="d1581-124">MainAccountCategory</span></span>              | <span data-ttu-id="d1581-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="d1581-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="d1581-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="d1581-126">MainAccount</span></span>                      | <span data-ttu-id="d1581-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="d1581-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="d1581-128">DK</span><span class="sxs-lookup"><span data-stu-id="d1581-128">Ledger</span></span>                           | <span data-ttu-id="d1581-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="d1581-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="d1581-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="d1581-130">ExchangeRates</span></span>                    | <span data-ttu-id="d1581-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="d1581-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="d1581-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="d1581-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="d1581-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="d1581-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="d1581-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="d1581-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="d1581-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="d1581-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="d1581-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="d1581-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="d1581-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="d1581-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="d1581-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="d1581-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="d1581-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="d1581-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]