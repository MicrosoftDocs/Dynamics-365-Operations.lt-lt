---
title: Produkto konfigūracijos modelio skaičiavimai
description: Šioje temoje aprašoma, kaip sukurti produkto konfigūracijos modulio atributų skaičiavimus
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829623"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="e7724-103">Produkto konfigūracijos modelio skaičiavimai</span><span class="sxs-lookup"><span data-stu-id="e7724-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7724-104">Šioje temoje aprašoma, kaip sukurti produkto konfigūracijos modulio atributų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="e7724-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e7724-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="e7724-105">Prerequisites</span></span>

<span data-ttu-id="e7724-106">Skaičiavimai yra naudojami produkto konfigūracijos modelyje, siekiant apskaičiuoti produkto konfigūracijos vertes.</span><span class="sxs-lookup"><span data-stu-id="e7724-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="e7724-107">Galėsite pradėti nustatyti skaičiavimus tik tuo atveju, jei egzistuos susijęs produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="e7724-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="e7724-108">Konfigūracijos modelių ir susijusių užduočių nustatymo proceso apžvalgą rasite [Produkto konfigūracijos modelio nustatymas](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="e7724-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="e7724-109">Skaičiavimo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="e7724-109">Create a calculation</span></span>

<span data-ttu-id="e7724-110">Skaičiavimą sudaro išraiška ir tikslinis atributas.</span><span class="sxs-lookup"><span data-stu-id="e7724-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="e7724-111">Daugiau informacijos rasite [Produktų konfigūracijos modelių skaičiavimų DUK](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="e7724-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="e7724-112">Norėdami sukurti skaičiavimą esamam produkto modeliui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7724-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="e7724-113">Eikite į **Produkto informacijos valdymas \> Bendra \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e7724-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="e7724-114">Atidarykite produkto konfigūracijos modelį ir tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e7724-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="e7724-115">„FastTab“ **Skaičiavimai** pasirinkite **Įtraukti** norėdami įtraukti skaičiavimą ir tada nustatykite šiuos laukus:</span><span class="sxs-lookup"><span data-stu-id="e7724-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="e7724-116">**Pavadinimas** – Įveskite skaičiavimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7724-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="e7724-117">**Aprašas** – Įveskite skaičiavimo aprašą.</span><span class="sxs-lookup"><span data-stu-id="e7724-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="e7724-118">**Tikslinis atributas** – Pasirinkite atributą, kuriam atliekate skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="e7724-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="e7724-119">Pasirinkite **Redaguoti išraišką**.</span><span class="sxs-lookup"><span data-stu-id="e7724-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="e7724-120">Dialogo lange **Įvesti skaičiavimą** į išraišką įtraukite reikiamus atributus, operatorius ir reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e7724-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="e7724-121">Daugiau informacijos apie tai, kaip dirbti su šiais elementais rasite [Išraiškos ir lentelių apribojimai produkto konfigūracijos modeliuose](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="e7724-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="e7724-122">Kai išraiška bus parengta, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e7724-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="e7724-123">Skaičiavimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="e7724-123">Calculation examples</span></span>

<span data-ttu-id="e7724-124">Šiame skyriuje pateikiami keli pavyzdžiai, kaip veikia skaičiavimai.</span><span class="sxs-lookup"><span data-stu-id="e7724-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="e7724-125">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e7724-125">Example 1</span></span>

<span data-ttu-id="e7724-126">Tikslinis atributas yra Bulio logika, o skaičiavime naudojama ši sąlyginė išraiška:</span><span class="sxs-lookup"><span data-stu-id="e7724-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="e7724-127">Išraiška pateikia tikslinio atributo reikšmę *Teisinga*, jei „`decimalAttribute2`” yra lygus arba didesnis nei `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="e7724-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="e7724-128">Kitu atveju išraiška grąžina Bulio logikos reikšmę *Klaidinga*.</span><span class="sxs-lookup"><span data-stu-id="e7724-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="e7724-129">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e7724-129">Example 2</span></span>

<span data-ttu-id="e7724-130">Šiame pavyzdyje teksto atributas „`textFixedList`” naudojamas kaip tikslo atributas.</span><span class="sxs-lookup"><span data-stu-id="e7724-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="e7724-131">Šį atributą sudaro toliau pateiktas fiksuotas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e7724-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="e7724-132">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="e7724-132">Value</span></span> | <span data-ttu-id="e7724-133">Sprendimo priemonės reikšmė</span><span class="sxs-lookup"><span data-stu-id="e7724-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="e7724-134">„A”</span><span class="sxs-lookup"><span data-stu-id="e7724-134">A</span></span> | <span data-ttu-id="e7724-135">„1a”</span><span class="sxs-lookup"><span data-stu-id="e7724-135">1a</span></span> |
| <span data-ttu-id="e7724-136">„B”</span><span class="sxs-lookup"><span data-stu-id="e7724-136">B</span></span> | <span data-ttu-id="e7724-137">„2b”</span><span class="sxs-lookup"><span data-stu-id="e7724-137">2b</span></span> |
| <span data-ttu-id="e7724-138">„C”</span><span class="sxs-lookup"><span data-stu-id="e7724-138">C</span></span> | <span data-ttu-id="e7724-139">„2c”</span><span class="sxs-lookup"><span data-stu-id="e7724-139">2c</span></span> |

<span data-ttu-id="e7724-140">Toliau pateiktoje ekrano kopijoje parodyta, kaip šio atributo parametrai gali atrodyti jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e7724-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="e7724-141">![Atributo tipo parametrai 2 pavyzdžiui](media/model-calculations-example2.png "Atributo tipo parametrai 2 pavyzdžiui")</span><span class="sxs-lookup"><span data-stu-id="e7724-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="e7724-142">Atributas yra naudojamas šiame sąlyginiame sakinyje:</span><span class="sxs-lookup"><span data-stu-id="e7724-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="e7724-143">Jei „`integerAttribute`” vertė yra mažesnė nei 150, šis sakinys grąžina pirmo įrašo fiksuotame sąraše tekstinę reikšmę *„A”*. Kitu atveju grąžinama trečio įrašo fiksuotame sąraše tekstinė reikšmė *„C”*.</span><span class="sxs-lookup"><span data-stu-id="e7724-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="e7724-144">Fiksuotas sąrašas yra nulinio išvardijimo („enum”) atitikmuo ir jo reikšmės pasiekiamos naudojant atitinkamą sveikojo skaičiaus vertę.</span><span class="sxs-lookup"><span data-stu-id="e7724-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="e7724-145">Todėl pirmoji fiksuota sąrašo reikšmė (*„A”*) sutapatinama *su 0*, o antroji reikšme (*„B”*) sutapatinama *su 1*, ir trečioji vertė (*„C”*) sutapatinama *su 2*.</span><span class="sxs-lookup"><span data-stu-id="e7724-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="e7724-146">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e7724-146">Example 3</span></span>

<span data-ttu-id="e7724-147">Šiame pavyzdyje naudojamas tikslinis atributas „`textFixedList`” iš ankstesnio pavyzdžio.</span><span class="sxs-lookup"><span data-stu-id="e7724-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="e7724-148">Taip pat naudojamas kitas teksto atributas, „`textAttribute`”, kuriame yra šis fiksuotas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e7724-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="e7724-149">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="e7724-149">Value</span></span> | <span data-ttu-id="e7724-150">Sprendimo priemonės reikšmė</span><span class="sxs-lookup"><span data-stu-id="e7724-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="e7724-151">„AA”</span><span class="sxs-lookup"><span data-stu-id="e7724-151">AA</span></span> | <span data-ttu-id="e7724-152">„1aa”</span><span class="sxs-lookup"><span data-stu-id="e7724-152">1aa</span></span> |
| <span data-ttu-id="e7724-153">„BB”</span><span class="sxs-lookup"><span data-stu-id="e7724-153">BB</span></span> | <span data-ttu-id="e7724-154">„2bb”</span><span class="sxs-lookup"><span data-stu-id="e7724-154">2bb</span></span> |

<span data-ttu-id="e7724-155">Toliau pateiktoje ekrano kopijoje parodyta, kaip šio atributo parametrai gali atrodyti jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e7724-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="e7724-156">![Atributo tipo parametrai 3 pavyzdžiui](media/model-calculations-example3.png "Atributo tipo parametrai 3 pavyzdžiui")</span><span class="sxs-lookup"><span data-stu-id="e7724-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="e7724-157">„`textFixedList`” atributo reikšmė apskaičiuojama naudojant šį sąlyginį sakinį:</span><span class="sxs-lookup"><span data-stu-id="e7724-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="e7724-158">Jei „`textAttribute`” reikšmė turi sprendimo priemonės reikšmę, lygią *„1aa”*, ši išraiška grąžina pirmo įrašo fiksuotame sąraše „`textFixedList`” tekstinę reikšmę *„A”*. Kitu atveju grąžinama trečio įrašo fiksuotame sąraše „`textFixedList`” tekstinė reikšmė *„C”*.</span><span class="sxs-lookup"><span data-stu-id="e7724-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="e7724-159">Sąlyginis sakinys turi naudoti atributo sprendimo priemonės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e7724-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="e7724-160">Skaičiavimuose galima naudoti tik fiksuoto sąrašo teksto atributus.</span><span class="sxs-lookup"><span data-stu-id="e7724-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7724-161">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="e7724-161">See also</span></span>

- [<span data-ttu-id="e7724-162">Produktų konfigūracijos modelių skaičiavimų DUK</span><span class="sxs-lookup"><span data-stu-id="e7724-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="e7724-163">Išraiškos apribojimo įtraukimas į produkto konfigūracijos modelį</span><span class="sxs-lookup"><span data-stu-id="e7724-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="e7724-164">Produkto konfigūracijos modelių apžvalga</span><span class="sxs-lookup"><span data-stu-id="e7724-164">Product configuration models overview</span></span>](product-configuration-models.md)
