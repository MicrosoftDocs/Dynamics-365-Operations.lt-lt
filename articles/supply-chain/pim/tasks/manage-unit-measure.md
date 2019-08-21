---
title: Tvarkyti matavimo vienetą
description: Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.
author: sorenva
manager: AnnBe
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 042a7495d55fb9d884771972cfc18e5ddb25330d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844326"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="84710-103">Tvarkyti matavimo vienetą</span><span class="sxs-lookup"><span data-stu-id="84710-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84710-104">Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="84710-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="84710-105">Šią procedūrą galite žingsnis po žingsnio atlikti naudodami demonstracinius duomenis arba savo pačių duomenis.</span><span class="sxs-lookup"><span data-stu-id="84710-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="84710-106">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Patvirtinto produkto priežiūra**.</span><span class="sxs-lookup"><span data-stu-id="84710-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="84710-107">Spustelėkite **Vienetai**.</span><span class="sxs-lookup"><span data-stu-id="84710-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="84710-108">Kurti matavimo vienetą</span><span class="sxs-lookup"><span data-stu-id="84710-108">Create a unit of measure</span></span>
1. <span data-ttu-id="84710-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="84710-109">Click **New**.</span></span>
2. <span data-ttu-id="84710-110">Lauke **Unit** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="84710-111">Įveskite ID arba simbolį, naudojamą nurodant matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="84710-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="84710-112">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="84710-113">Įveskite matavimo vieneto aprašomąjį pavadinimą sistemos kalba.</span><span class="sxs-lookup"><span data-stu-id="84710-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="84710-114">Lauke **Vieneto klasė** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="84710-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="84710-115">Vieneto klasė apibrėžia, kokiai loginei grupei, pvz., plotui, masei ar kiekiui, priklauso matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="84710-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="84710-116">Lauke **Dešimtainis tikslumas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="84710-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="84710-117">Nurodykite dešimtainių dalių skaičių, iki kurio turi būti apvalinamas konvertuojamas matavimo vienetas atlikus skaičiavimą su šiuo matavimo vienetu.</span><span class="sxs-lookup"><span data-stu-id="84710-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="84710-118">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="84710-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="84710-119">Apibrėžti vieneto vertimus</span><span class="sxs-lookup"><span data-stu-id="84710-119">Define unit translations</span></span>
1. <span data-ttu-id="84710-120">**Action pane** spustelėkite **Unit texts**.</span><span class="sxs-lookup"><span data-stu-id="84710-120">On the **Action pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="84710-121">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="84710-121">Click **New**.</span></span> <span data-ttu-id="84710-122">Naudodami vieneto tekstą sukurkite matavimo vienetą reprezentuojančio ID arba simbolio vertimą, kuris bus naudojamas išoriniuose dokumentuose konkretaus kliento arba tiekėjo kalbomis.</span><span class="sxs-lookup"><span data-stu-id="84710-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="84710-123">Lauke **Kalba** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="84710-124">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="84710-125">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="84710-125">Click **Save**.</span></span>
6. <span data-ttu-id="84710-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="84710-126">Close the page.</span></span>
7. <span data-ttu-id="84710-127">**Action pane** spustelėkite **Translated unit descriptions**.</span><span class="sxs-lookup"><span data-stu-id="84710-127">On the **Action pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="84710-128">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="84710-128">Click **New**.</span></span> <span data-ttu-id="84710-129">Nurodykite matavimo vieneto aprašus konkrečia kalba.</span><span class="sxs-lookup"><span data-stu-id="84710-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="84710-130">Lauke **Kalba** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="84710-131">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="84710-132">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="84710-132">Click **Save**.</span></span>
12. <span data-ttu-id="84710-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="84710-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="84710-134">Apibrėžti vieneto konvertavimo taisykles</span><span class="sxs-lookup"><span data-stu-id="84710-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="84710-135">**Action pane** spustelėkite **Unit conversions**.</span><span class="sxs-lookup"><span data-stu-id="84710-135">On the **Action pane**, click **Unit conversions**.</span></span> <span data-ttu-id="84710-136">Apibrėžkite matavimo vieneto konvertavimo į ir iš kitų matavimo vienetų pasirinktoje vieneto klasėje taisykles.</span><span class="sxs-lookup"><span data-stu-id="84710-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="84710-137">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="84710-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="84710-138">Lauke **Koeficientas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="84710-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="84710-139">Konvertavimo iš vienetų į vienetus koeficientas.</span><span class="sxs-lookup"><span data-stu-id="84710-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="84710-140">Pvz., konvertavimo iš centimetrus į metrus koeficientas yra 100, nes vienas metras turi 100 centimetrų.</span><span class="sxs-lookup"><span data-stu-id="84710-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="84710-141">Lauke **Į vnt.** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84710-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="84710-142">Lauke **Apvalinimas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="84710-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="84710-143">Apibrėžkite, kaip turi būti apvalinama konvertuota reikšmė.</span><span class="sxs-lookup"><span data-stu-id="84710-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="84710-144">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="84710-144">Click **OK**.</span></span>
7. <span data-ttu-id="84710-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="84710-145">Close the page.</span></span>

