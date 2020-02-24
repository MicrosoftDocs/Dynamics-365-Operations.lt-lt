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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019919"
---
# <a name="integrated-ledger"></a><span data-ttu-id="d2c43-103">Integruota didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="d2c43-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="d2c43-104">Verslo programoje didžiosios knygos duomenimis nustatoma pagrindinė sąranka, kaip įmonė vykdo veiklą.</span><span class="sxs-lookup"><span data-stu-id="d2c43-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="d2c43-105">Pavyzdžiui, didžiosios knygos duomenimis nurodomi finansiniai metai, kurių įmonė laikosi, valiutos, kuriomis ji atlieka operacijas, ir naudojamos sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="d2c43-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="d2c43-106">Šioje temoje aprašomas šių pagrindinių finansinių duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="d2c43-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="d2c43-107">Šablonai</span><span class="sxs-lookup"><span data-stu-id="d2c43-107">Templates</span></span>

<span data-ttu-id="d2c43-108">Didžiosios knygos duomenis sudaro pagrindinių finansinių objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="d2c43-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="d2c43-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="d2c43-109">Finance and Operations apps</span></span>      | <span data-ttu-id="d2c43-110">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="d2c43-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="d2c43-111">Valiutos</span><span class="sxs-lookup"><span data-stu-id="d2c43-111">Currencies</span></span>                       | <span data-ttu-id="d2c43-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="d2c43-112">transactioncurrencies</span></span>
<span data-ttu-id="d2c43-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="d2c43-113">FiscalCalendar</span></span>                   | <span data-ttu-id="d2c43-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="d2c43-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="d2c43-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="d2c43-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="d2c43-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="d2c43-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="d2c43-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="d2c43-117">ExchRateType</span></span>                     | <span data-ttu-id="d2c43-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="d2c43-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="d2c43-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="d2c43-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="d2c43-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="d2c43-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="d2c43-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="d2c43-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="d2c43-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="d2c43-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="d2c43-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="d2c43-123">MainAccountCategory</span></span>              | <span data-ttu-id="d2c43-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="d2c43-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="d2c43-125">MainAccount</span><span class="sxs-lookup"><span data-stu-id="d2c43-125">MainAccount</span></span>                      | <span data-ttu-id="d2c43-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="d2c43-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="d2c43-127">DK</span><span class="sxs-lookup"><span data-stu-id="d2c43-127">Ledger</span></span>                           | <span data-ttu-id="d2c43-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="d2c43-128">msdyn\_ledgers</span></span>
<span data-ttu-id="d2c43-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="d2c43-129">ExchangeRates</span></span>                    | <span data-ttu-id="d2c43-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="d2c43-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="d2c43-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="d2c43-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="d2c43-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="d2c43-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="d2c43-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="d2c43-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="d2c43-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="d2c43-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="d2c43-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="d2c43-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="d2c43-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="d2c43-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="d2c43-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="d2c43-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="d2c43-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="d2c43-138">msdyn\_chartofaccounts.md</span></span>


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




