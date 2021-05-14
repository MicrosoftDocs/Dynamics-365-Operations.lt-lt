---
title: Prekių kokybės tikrinimas
description: Šioje temoje paaiškinama, kaip apdoroti kokybės užsakymus.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956139"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="fb11e-103">Prekių kokybės tikrinimas</span><span class="sxs-lookup"><span data-stu-id="fb11e-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb11e-104">Šioje temoje paaiškinama, kaip apdoroti kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="fb11e-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="fb11e-105">Kokybės patikrinimus paprastai atlieka kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="fb11e-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="fb11e-106">Jei įdiegti standartiniai demonstraciniai duomenys, galite naudoti juos šios temos procedūroms atlikti.</span><span class="sxs-lookup"><span data-stu-id="fb11e-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="fb11e-107">Norėdami naudoti demonstracinius duoemnis, pasirinkite *„USMF”* juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="fb11e-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="fb11e-108">Tada turite patvirtinti pirkimo užsakymą *000016* ir užregistruoti produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="fb11e-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="fb11e-109">Kokybės užsakymas generuojamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="fb11e-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="fb11e-110">1 veiksmas: Pasirinkti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="fb11e-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="fb11e-111">Norėdami pasirinkti kokybės užsakymą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb11e-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="fb11e-112">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="fb11e-113">Pasirinkite kokybės užsakymą, sukurtą prieš jums pradedant šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="fb11e-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="fb11e-114">2 veiksmas: Įrašyti tikrinimo rezultatus</span><span class="sxs-lookup"><span data-stu-id="fb11e-114">Step 2: Record test results</span></span>

<span data-ttu-id="fb11e-115">Norėdami įrašyti tikrinimo rezultatus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb11e-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="fb11e-116">Pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-116">Select **Results**.</span></span>
1. <span data-ttu-id="fb11e-117">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-117">Select **Edit**.</span></span>
1. <span data-ttu-id="fb11e-118">Lauke **Rezultatų kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fb11e-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="fb11e-119">Lauke **Išvados** pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="fb11e-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="fb11e-120">Šiame pavyzdyje rezultatas priklauso nuo iš anksto nustatytos baigties.</span><span class="sxs-lookup"><span data-stu-id="fb11e-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="fb11e-121">Paprastai įrašomas konkretesnis bandymo rezultatas, pavyzdžiui, dydis ar kitas matmuo.</span><span class="sxs-lookup"><span data-stu-id="fb11e-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="fb11e-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-122">Select **Save**.</span></span>
1. <span data-ttu-id="fb11e-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb11e-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="fb11e-124">3 veiksmas: Tikrinti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="fb11e-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="fb11e-125">Norėdami patvirtinti kokybės užsakymą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb11e-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="fb11e-126">Pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-126">Select **Validate**.</span></span>
1. <span data-ttu-id="fb11e-127">Lauke **Patvirtinta pagal** pasirinkite vartotoją, kuris atlieka patikrinimą.</span><span class="sxs-lookup"><span data-stu-id="fb11e-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="fb11e-128">Pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-128">Select **Select**.</span></span>
1. <span data-ttu-id="fb11e-129">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fb11e-129">Select **OK**.</span></span>
1. <span data-ttu-id="fb11e-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb11e-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
