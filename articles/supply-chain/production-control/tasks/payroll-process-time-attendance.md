---
title: Įgalinti laiko ir buvimo darbe algalapio procesą
description: Ši procedūra parodo, kaip įgalinti laiko ir buvimo darbe algalapio procesą.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72b925feb8f784c257656dd93b48c9c0cc66da5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214919"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="ec7d7-103">Įgalinti laiko ir buvimo darbe algalapio procesą</span><span class="sxs-lookup"><span data-stu-id="ec7d7-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec7d7-104">Ši procedūra parodo, kaip įgalinti laiko ir buvimo darbe algalapio procesą.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="ec7d7-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="ec7d7-106">Kurti mokėjimo tipą su susijusiu darbo užmokesčio tarifu</span><span class="sxs-lookup"><span data-stu-id="ec7d7-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="ec7d7-107">Laikas ir buvimas darbe > Nustatymas > Algalapis > Mokėjimo tipai</span><span class="sxs-lookup"><span data-stu-id="ec7d7-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="ec7d7-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-108">Click New.</span></span>
3. <span data-ttu-id="ec7d7-109">Lauke Mokėjimo tipas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="ec7d7-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec7d7-111">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-111">Click Save.</span></span>
6. <span data-ttu-id="ec7d7-112">Spustelėkite Tarifai.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-112">Click Rates.</span></span>
    * <span data-ttu-id="ec7d7-113">Mokėjimo tipų koeficientai nustatomi tam tikriems laiko intervalams, o darbuotojams gali būti sukurti atskiri koeficientai.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="ec7d7-114">Ne visada būtina kurti laiko ir buvimo darbe mokėjimo tipų koeficientus.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="ec7d7-115">Ši informacija jau gali būti algalapių sistemoje, kuri naudojama atlyginimams generuoti.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="ec7d7-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-116">Click New.</span></span>
8. <span data-ttu-id="ec7d7-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ec7d7-118">Lauke Tarifas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="ec7d7-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="ec7d7-120">Mokėjimo sutarties kūrimas</span><span class="sxs-lookup"><span data-stu-id="ec7d7-120">Create a pay agreement</span></span>
1. <span data-ttu-id="ec7d7-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-121">Close the page.</span></span>
2. <span data-ttu-id="ec7d7-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-122">Close the page.</span></span>
3. <span data-ttu-id="ec7d7-123">Eikite į Mokėjimo sutartys.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="ec7d7-124">Laikas ir buvimas darbe > Nustatymas > Mokėjimo sutartys</span><span class="sxs-lookup"><span data-stu-id="ec7d7-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="ec7d7-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-125">Click New.</span></span>
5. <span data-ttu-id="ec7d7-126">Lauke Mokėjimo sutartis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="ec7d7-127">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="ec7d7-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-128">Click Save.</span></span>
8. <span data-ttu-id="ec7d7-129">Spustelėkite Sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="ec7d7-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-130">Click New.</span></span>
10. <span data-ttu-id="ec7d7-131">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ec7d7-132">Lauke Profilio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="ec7d7-133">Lauke Mokėjimo tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="ec7d7-134">Nustatyti laiko ir registracijos darbuotojo mokėjimo sutartį</span><span class="sxs-lookup"><span data-stu-id="ec7d7-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="ec7d7-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-135">Close the page.</span></span>
2. <span data-ttu-id="ec7d7-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-136">Close the page.</span></span>
3. <span data-ttu-id="ec7d7-137">Eikite į Laiko registracijos darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="ec7d7-138">Laikas ir buvimas darbe > Nustatymas > Laiko registracijos darbuotojai</span><span class="sxs-lookup"><span data-stu-id="ec7d7-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="ec7d7-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ec7d7-140">Spustelėkite skirtuką Užimtumas.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="ec7d7-141">Išplėskite skyrių Laiko registracija.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="ec7d7-142">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-142">Click Edit.</span></span>
8. <span data-ttu-id="ec7d7-143">Lauke Mokėjimo sutartis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-143">In the Pay agreement field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]