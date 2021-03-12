---
title: Tvarkyti matavimo vienetą
description: Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71b478ca294719c20af9de16c27139aeca36bf07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992300"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="b6d71-103">Tvarkyti matavimo vienetą</span><span class="sxs-lookup"><span data-stu-id="b6d71-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6d71-104">Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="b6d71-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="b6d71-105">Šią procedūrą galite žingsnis po žingsnio atlikti naudodami demonstracinius duomenis arba savo pačių duomenis.</span><span class="sxs-lookup"><span data-stu-id="b6d71-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="b6d71-106">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Patvirtinto produkto priežiūra**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="b6d71-107">Spustelėkite **Vienetai**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="b6d71-108">Kurti matavimo vienetą</span><span class="sxs-lookup"><span data-stu-id="b6d71-108">Create a unit of measure</span></span>
1. <span data-ttu-id="b6d71-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-109">Click **New**.</span></span>
2. <span data-ttu-id="b6d71-110">Lauke **Vienetas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="b6d71-111">Įveskite ID arba simbolį, naudojamą nurodant matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="b6d71-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="b6d71-112">Lauke **Aprašymas įveskite** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="b6d71-113">Įveskite matavimo vieneto aprašomąjį pavadinimą sistemos kalba.</span><span class="sxs-lookup"><span data-stu-id="b6d71-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="b6d71-114">Lauke **Vieneto klasė** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b6d71-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="b6d71-115">Vieneto klasė apibrėžia, kokiai loginei grupei, pvz., plotui, masei ar kiekiui, priklauso matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="b6d71-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="b6d71-116">Lauke **Dešimtainis tikslumas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b6d71-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="b6d71-117">Nurodykite dešimtainių dalių skaičių, iki kurio turi būti apvalinamas konvertuojamas matavimo vienetas atlikus skaičiavimą su šiuo matavimo vienetu.</span><span class="sxs-lookup"><span data-stu-id="b6d71-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="b6d71-118">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="b6d71-119">Apibrėžti vieneto vertimus</span><span class="sxs-lookup"><span data-stu-id="b6d71-119">Define unit translations</span></span>
1. <span data-ttu-id="b6d71-120">**Veiksmų srityje** spustelėkite **Vieneto tekstai**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="b6d71-121">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-121">Click **New**.</span></span> <span data-ttu-id="b6d71-122">Naudodami vieneto tekstą sukurkite matavimo vienetą reprezentuojančio ID arba simbolio vertimą, kuris bus naudojamas išoriniuose dokumentuose konkretaus kliento arba tiekėjo kalbomis.</span><span class="sxs-lookup"><span data-stu-id="b6d71-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="b6d71-123">Lauke **Kalba** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="b6d71-124">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="b6d71-125">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-125">Click **Save**.</span></span>
6. <span data-ttu-id="b6d71-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6d71-126">Close the page.</span></span>
7. <span data-ttu-id="b6d71-127">**Veiksmų srityje** spustelėkite **Išversti vienetų aprašai**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="b6d71-128">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-128">Click **New**.</span></span> <span data-ttu-id="b6d71-129">Nurodykite matavimo vieneto aprašus konkrečia kalba.</span><span class="sxs-lookup"><span data-stu-id="b6d71-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="b6d71-130">Lauke **Kalba** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="b6d71-131">Lauke **Aprašymas įveskite** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="b6d71-132">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-132">Click **Save**.</span></span>
12. <span data-ttu-id="b6d71-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6d71-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="b6d71-134">Apibrėžti vieneto konvertavimo taisykles</span><span class="sxs-lookup"><span data-stu-id="b6d71-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="b6d71-135">**Veiksmų srityje** spustelėkite **Vienetų konvertavimas**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="b6d71-136">Apibrėžkite matavimo vieneto konvertavimo į ir iš kitų matavimo vienetų pasirinktoje vieneto klasėje taisykles.</span><span class="sxs-lookup"><span data-stu-id="b6d71-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="b6d71-137">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b6d71-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="b6d71-138">Lauke **Koeficientas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b6d71-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="b6d71-139">Konvertavimo iš vienetų į vienetus koeficientas.</span><span class="sxs-lookup"><span data-stu-id="b6d71-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="b6d71-140">Pvz., konvertavimo iš centimetrus į metrus koeficientas yra 100, nes vienas metras turi 100 centimetrų.</span><span class="sxs-lookup"><span data-stu-id="b6d71-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="b6d71-141">Lauke **Į vnt.** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d71-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="b6d71-142">Lauke **Apvalinimas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b6d71-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="b6d71-143">Apibrėžkite, kaip turi būti apvalinama konvertuota reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b6d71-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="b6d71-144">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b6d71-144">Click **OK**.</span></span>
7. <span data-ttu-id="b6d71-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6d71-145">Close the page.</span></span>

