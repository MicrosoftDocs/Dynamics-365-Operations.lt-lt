---
title: Mokesčių skaičiavimo efektyvumas veikia operacijas
description: Šioje temoje pateikiama trikčių diagnostikos informacija, susijusi su mokesčių skaičiavimo našumui ir jos poveikis operacijoms.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947683"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="a79d2-103">Mokesčių skaičiavimo efektyvumas veikia operacijas</span><span class="sxs-lookup"><span data-stu-id="a79d2-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a79d2-104">Kartais operacijai daro įtakos našumo problemos, kurias turi mokesčių skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="a79d2-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="a79d2-105">Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a79d2-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="a79d2-106">Peržiūrėti perlaidos eilutės skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="a79d2-106">Review the transaction line count</span></span>

<span data-ttu-id="a79d2-107">Nustatykite, ar operacijoje yra daug eilučių (pvz., daugiau nei keli šimtai).</span><span class="sxs-lookup"><span data-stu-id="a79d2-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="a79d2-108">Jei nėra, pereisite į kitą skyrių.</span><span class="sxs-lookup"><span data-stu-id="a79d2-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="a79d2-109">Jei operacijoje yra keli šimtai eilučių, atidėti mokesčių skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a79d2-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="a79d2-110">Daugiau informacijos rasite Įgalinti [atidėtų mokesčių skaičiavimą](enable-delayed-tax-calculation.md) žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="a79d2-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="a79d2-111">Po to galite nustatyti, ar įvykdyta kuri nors iš šių sąlygų:</span><span class="sxs-lookup"><span data-stu-id="a79d2-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="a79d2-112">Yra importavimo operacijų iš didelių failų.</span><span class="sxs-lookup"><span data-stu-id="a79d2-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="a79d2-113">Keli seansai vienu metu apdoros tą patį operacijos mokesčio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a79d2-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="a79d2-114">Operacijoje yra kelios eilutės, o rodiniai atnaujinami tikru laiku.</span><span class="sxs-lookup"><span data-stu-id="a79d2-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="a79d2-115">Pvz., laukas Apskaičiuota PVM suma, pateiktas bendrojo žurnalo puslapyje, yra atnaujinamas realiuoju laiku, **kai** pakeičiami eilutės **laukai**.</span><span class="sxs-lookup"><span data-stu-id="a79d2-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="a79d2-116">[![Apskaičiuotas PVM sumos laukas Jounal kvito puslapyje](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="a79d2-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="a79d2-117">Jei įvykdyta kuri nors iš šių sąlygų, atidėti mokesčių skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a79d2-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="a79d2-118">Peržiūrėti iškvietimų dėklą</span><span class="sxs-lookup"><span data-stu-id="a79d2-118">Review the call stack</span></span>

<span data-ttu-id="a79d2-119">Peržiūrėti iškvietimų dėklą ir nustatyti, ar mokesčių skaičiavimas iškviestas kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="a79d2-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="a79d2-120">Jei jo nėra, pereisite į kitą skyrių.</span><span class="sxs-lookup"><span data-stu-id="a79d2-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="a79d2-121">Jei iškvietimų dėklas iškviestas kelis kartus, atlikite šiuos veiksmus ir taip sumažinsite mokesčių skaičiavimo laiką.</span><span class="sxs-lookup"><span data-stu-id="a79d2-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="a79d2-122">Jei į žurnalą atsižvelgta į operaciją, atidėti mokesčio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a79d2-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="a79d2-123">Daugiau informacijos rasite Įgalinti [atidėtų mokesčių skaičiavimą](enable-delayed-tax-calculation.md) žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="a79d2-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="a79d2-124">Jei operacija yra pirkimo užsakymas, o programos versija vėlesnė nei 10.0.15, galite atidėti mokesčių skaičiavimą iki galutinio skaičiavimo, įjungdami atėjimo **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="a79d2-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="a79d2-125">Peržiūrėti iškvietimų dėklo laiko juosta</span><span class="sxs-lookup"><span data-stu-id="a79d2-125">Review the call stack timeline</span></span>

<span data-ttu-id="a79d2-126">Peržiūrėkite iškvietimų dėklo laiko juostą, kad nustatytumėte, ar yra tokių problemų.</span><span class="sxs-lookup"><span data-stu-id="a79d2-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="a79d2-127">Jei taip ir yra, įjunkite **TaxUncommittedDoIsolateFreFlighting skrydžio funkciją,** kad išspręstumėte problemą.</span><span class="sxs-lookup"><span data-stu-id="a79d2-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="a79d2-128">Dėl operacijos sistema nustoja reaguoti, kol seansas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a79d2-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="a79d2-129">Todėl operacija negali apskaičiuoti mokesčio rezultato.</span><span class="sxs-lookup"><span data-stu-id="a79d2-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="a79d2-130">Šioje iliustracijoje rodomas jūsų gauti pranešimų langas „Seansas baigtas".</span><span class="sxs-lookup"><span data-stu-id="a79d2-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="a79d2-131">[![Pranešimas apie seansą](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="a79d2-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="a79d2-132">**TaxUncommitted metodai** užtruko daugiau laiko nei kiti metodai.</span><span class="sxs-lookup"><span data-stu-id="a79d2-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="a79d2-133">Pavyzdžiui, pagal šį pavyzdį **TaxUncommitted ::updateTaxUncommitted() metodas trunka 43 347,42 sekundėmis, tačiau kiti metodai** užtrunka 0,09 sekundės.</span><span class="sxs-lookup"><span data-stu-id="a79d2-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="a79d2-134">[![Metodo trukmė](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="a79d2-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="a79d2-135">Mokesčių skaičiavimo tinkinimas ir iškviečiamas</span><span class="sxs-lookup"><span data-stu-id="a79d2-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="a79d2-136">Kai pritaikote, nekviesti mokesčių skaičiavimo **įterpimo()** ar **update()** metodo kiekvienai eilutei.</span><span class="sxs-lookup"><span data-stu-id="a79d2-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="a79d2-137">Mokesčių skaičiavimas turi būti iškviestas operacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="a79d2-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="a79d2-138">Nustatyti, ar yra tinkinimas</span><span class="sxs-lookup"><span data-stu-id="a79d2-138">Determine whether customization exists</span></span>

<span data-ttu-id="a79d2-139">Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas.</span><span class="sxs-lookup"><span data-stu-id="a79d2-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="a79d2-140">Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.</span><span class="sxs-lookup"><span data-stu-id="a79d2-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
