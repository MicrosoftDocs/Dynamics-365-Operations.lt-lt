---
title: Produkto konfigūratoriaus trikties šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto konfigūratoriumi.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dacc7205eaf2084f6fbd3be9d8ac0572f9e1bcde
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516839"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="ea965-103">Produkto konfigūratoriaus trikties šalinimas</span><span class="sxs-lookup"><span data-stu-id="ea965-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="ea965-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto konfigūratoriumi.</span><span class="sxs-lookup"><span data-stu-id="ea965-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="ea965-105">Prekės tekstas yra užrašomas man konfigūruojant produktą prekybos užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ea965-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ea965-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="ea965-106">Issue description</span></span>

<span data-ttu-id="ea965-107">Ši klaida įvyksta jums kuriant prekybos užsakymo eilutę konfigūruojamoje prekėje ir tuomet keičiant prekės tekstą.</span><span class="sxs-lookup"><span data-stu-id="ea965-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="ea965-108">Jums konfigūruojant prekę ir tada pasirenktant **Gerai**, tekstas yra užrašomas standartiniu tekstu.</span><span class="sxs-lookup"><span data-stu-id="ea965-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ea965-109">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="ea965-109">Issue resolution</span></span>

<span data-ttu-id="ea965-110">Tikimasi tokio elgesio.</span><span class="sxs-lookup"><span data-stu-id="ea965-110">This behavior is expected.</span></span> <span data-ttu-id="ea965-111">Teksto laukelis apima varianto pavadinimą, kuris užpildomas tik po to kai sukonfigūruojate eilutę.</span><span class="sxs-lookup"><span data-stu-id="ea965-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="ea965-112">Dėl to, privalote keisti tekstą jums sukonfigūravus eilutę, o ne prieš tai.</span><span class="sxs-lookup"><span data-stu-id="ea965-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="ea965-113">Integruotojo savybės nėra tinkamai suapvalintos, kai produkto konfigūravimo modeliai yra skaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="ea965-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ea965-114">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="ea965-114">Issue description</span></span>

<span data-ttu-id="ea965-115">Ši problema atsitinka jums atliekant tolesnes veiksmų tvarkas:</span><span class="sxs-lookup"><span data-stu-id="ea965-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="ea965-116">Nustatykite tolesnius atributus gamybos konfigūravimo modelyje:</span><span class="sxs-lookup"><span data-stu-id="ea965-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="ea965-117">Įvestis (integruotojas)</span><span class="sxs-lookup"><span data-stu-id="ea965-117">Input (integer)</span></span>
    - <span data-ttu-id="ea965-118">Procentas (dešimtainis)</span><span class="sxs-lookup"><span data-stu-id="ea965-118">Percent (decimal)</span></span>
    - <span data-ttu-id="ea965-119">Rezultatas (integruotojas)</span><span class="sxs-lookup"><span data-stu-id="ea965-119">Result (integer)</span></span>

2. <span data-ttu-id="ea965-120">Sukurkite skaičiavimą, kuris turi tolesnes išraiškas:</span><span class="sxs-lookup"><span data-stu-id="ea965-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="ea965-121">*Rezultatas* = *Įvestis* × *Procentas* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="ea965-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="ea965-122">Tokiu atveju, integravimo rezultatas nėra visada tinkamai suapvalintas.</span><span class="sxs-lookup"><span data-stu-id="ea965-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="ea965-123">Pavyzdžiui, įvestis yra 1 000, o procentas yra 2,40.</span><span class="sxs-lookup"><span data-stu-id="ea965-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="ea965-124">Dėl to, tikitės integravimo rezultatų 24, nes 2,40 procentas 1 000 yra 24 (ar 24,00 dešimtaine forma).</span><span class="sxs-lookup"><span data-stu-id="ea965-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="ea965-125">Vietoje to, rodomas rezultatas yra 23.</span><span class="sxs-lookup"><span data-stu-id="ea965-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="ea965-126">Nepaisant to, kai procentas yra 2,39, skaičiavimas yra suapvalintas iki 24, o ne 23.</span><span class="sxs-lookup"><span data-stu-id="ea965-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="ea965-127">Kai procentas yra 2,50, skaičiavimas yra suapvalintas iki 25 kaip tikėtasi.</span><span class="sxs-lookup"><span data-stu-id="ea965-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ea965-128">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="ea965-128">Issue resolution</span></span>

<span data-ttu-id="ea965-129">Ši problema atsitinka dažnai, nes „Microsoft Solver Foundation“ pati programa turi skaičius naudodama frakcijas.</span><span class="sxs-lookup"><span data-stu-id="ea965-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="ea965-130">Ankstesniame pavyzdyje, skaičiavimo rezultatas, kai 2,40 procentas yra rodomas kaip 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="ea965-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="ea965-131">Kai .NET rodo integruojamą vertę, ji grįš 23.</span><span class="sxs-lookup"><span data-stu-id="ea965-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="ea965-132">Šis elgesys nepasikeis, nes kiti scenarijai nuo jo priklauso.</span><span class="sxs-lookup"><span data-stu-id="ea965-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="ea965-133">Ankstesniame pavyzdyje, galite ištaisyti problemą įvesdami papildomus dešimtainius atributus ir skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="ea965-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="ea965-134">Pavyzdžiui, galite nustatyti tolesnius atributus gamybos konfigūravimo modelyje:</span><span class="sxs-lookup"><span data-stu-id="ea965-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="ea965-135">Įvestis (integruotojas)</span><span class="sxs-lookup"><span data-stu-id="ea965-135">Input (integer)</span></span>
- <span data-ttu-id="ea965-136">Procentas (dešimtainis)</span><span class="sxs-lookup"><span data-stu-id="ea965-136">Percent (decimal)</span></span>
- <span data-ttu-id="ea965-137">Dešimtainis rezultatas (dešimtainis)</span><span class="sxs-lookup"><span data-stu-id="ea965-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="ea965-138">Rezultato integruotojas (integruotojas)</span><span class="sxs-lookup"><span data-stu-id="ea965-138">ResultInteger (integer)</span></span>

<span data-ttu-id="ea965-139">Tuomet galite įtraukti tolesnius apskaičiavimus:</span><span class="sxs-lookup"><span data-stu-id="ea965-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="ea965-140">*Dešimtainis rezultatas* = *Įvestis* × *Procentas* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="ea965-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="ea965-141">*Rezultato integruotojas* = *Dešimtainis rezultatas*</span><span class="sxs-lookup"><span data-stu-id="ea965-141">*ResultInteger* = *ResultDecimal*</span></span>
