---
title: Kokybės valdymo bandymai
description: Šioje temoje aprašoma, kaip sukurti bandymus, kuriuos galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021689"
---
# <a name="quality-management-tests"></a><span data-ttu-id="995c9-103">Kokybės valdymo bandymai</span><span class="sxs-lookup"><span data-stu-id="995c9-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="995c9-104">Šioje temoje aprašoma, kaip sukurti bandymus, kuriuos galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.</span><span class="sxs-lookup"><span data-stu-id="995c9-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="995c9-105">Naudokite **Bandymų** puslapį atskiriems tikrinimams, kuriais nustatoma, ar produktai atitinka kokybės reikalavimus, nustatyti ir peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="995c9-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="995c9-106">Bandymų grupei galite priskirti vieną arba kelis atskirus bandymus.</span><span class="sxs-lookup"><span data-stu-id="995c9-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="995c9-107">Šiuo atveju taip pat nurodote konkretaus bandymo informaciją, pvz., priimtinas matavimo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="995c9-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="995c9-108">Matavimo vertės naudojamos kiekybės bandymams.</span><span class="sxs-lookup"><span data-stu-id="995c9-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="995c9-109">Kokybinių bandymų metu naudojami bandymo kintamieji.</span><span class="sxs-lookup"><span data-stu-id="995c9-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="995c9-110">Kiekybės bandymams **lauke Tipas nustatoma vertė** Sveikas *skaičius* arba *Trupmena*.</span><span class="sxs-lookup"><span data-stu-id="995c9-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="995c9-111">Matavimo vienetas taip pat nurodomas.</span><span class="sxs-lookup"><span data-stu-id="995c9-111">A unit of measure is also specified.</span></span> <span data-ttu-id="995c9-112">Kokybės specifikacijos ir bandymų rezultatai išreiškiami skaičiais.</span><span class="sxs-lookup"><span data-stu-id="995c9-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="995c9-113">Kokybinių bandymų tipą turite **Tipo** laukelį nustatyti į *Pasirenkamas*.</span><span class="sxs-lookup"><span data-stu-id="995c9-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="995c9-114">Kokybės bandymams reikia pateikti papildomos informacijos apie bandymų kintamąjį, kuris vertinamas ir jo sunumeruotas parinktis.</span><span class="sxs-lookup"><span data-stu-id="995c9-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="995c9-115">Kokybės specifikacijos ir bandymų rezultatai išreiškiami atsižvelgiant į rezultatą.</span><span class="sxs-lookup"><span data-stu-id="995c9-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="995c9-116">Tikrinimo prietaisą taip pat galite pasirinktinai tikrinimo sričiai.</span><span class="sxs-lookup"><span data-stu-id="995c9-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="995c9-117">Tačiau tikrinimo priemonėms nereikia kurti ir naudoti bandymų su kokybės užsakymais.</span><span class="sxs-lookup"><span data-stu-id="995c9-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="995c9-118">Daugiau informacijos ieškokite Kokybės [valdymo tikrinimo](quality-test-instruments.md) priemonės.</span><span class="sxs-lookup"><span data-stu-id="995c9-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="995c9-119">Taip pat galite pasirinktinai nurodyti tikrinimo vienetą, norėdami nurodyti matavimo vienetą, į kurį įrašomi tikrinimo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="995c9-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="995c9-120">Pavyzdžiui, temperatūros tikrinimas gali apimti arba Farenheit, arba Ttsijaus laipsnių vienetą.</span><span class="sxs-lookup"><span data-stu-id="995c9-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="995c9-121">Bandymo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="995c9-121">Example of a test</span></span>

<span data-ttu-id="995c9-122">Gamybos įmonė atlieka du įsigytų medžiagų bandymus: kiekybinį bandymą dėl medžiagos kokybės ir kokybinį bandymą dėl pakuotės sugadinimo.</span><span class="sxs-lookup"><span data-stu-id="995c9-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="995c9-123">Įmonė nurodo papildomos informacijos, susijusios su kokybės tikrinimu, pateikdama tikrinimo kintamąjį (pavyzdžiui, pažeista pakuotė) ir jo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="995c9-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="995c9-124">Įmonė naudoja **Bandymų grupių** puslapį, kad bandymų grupei priskirtų šiuos du bandymus ir nurodytų konkretaus bandymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="995c9-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="995c9-125">Tikrinimų grupė priskiriama kokybės užsakymui tam, kad įmonė galėtų pateikti dviejų tikrinimų rezultatų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="995c9-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="995c9-126">Kurti bandymą</span><span class="sxs-lookup"><span data-stu-id="995c9-126">Create a test</span></span>

<span data-ttu-id="995c9-127">Atlikite šiuos žingsnius, kad sukurtumėte bandymą.</span><span class="sxs-lookup"><span data-stu-id="995c9-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="995c9-128">Eikite į **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Bandymai**.</span><span class="sxs-lookup"><span data-stu-id="995c9-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="995c9-129">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="995c9-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="995c9-130">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="995c9-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="995c9-131">**Bandymo instrumentas** – įveskite unikalų tikrinimo prietaiso ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="995c9-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="995c9-132">**Aprašas** – įveskite išsamų bandymo instrumento aprašą.</span><span class="sxs-lookup"><span data-stu-id="995c9-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="995c9-133">**Tipas** – pasirinkite rezultatų, kuriuos testas duoda, tipą.</span><span class="sxs-lookup"><span data-stu-id="995c9-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="995c9-134">Kiekybės bandymams pasirinkite *Trupmena* *arba sveikasis skaičius*.</span><span class="sxs-lookup"><span data-stu-id="995c9-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="995c9-135">Kokybinių bandymų atveju pasirinkite *Parinktį*.</span><span class="sxs-lookup"><span data-stu-id="995c9-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="995c9-136">**Tikrinimo prietaisas** – pasirinkite [tikrinimo](quality-test-instruments.md) prietaisą, kuris turi būti naudojamas bandymams.</span><span class="sxs-lookup"><span data-stu-id="995c9-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="995c9-137">**Vienetas** – Jei pasirinkote *Frakcija* ar *Sveikasis skaičius* lauke **Tipas** (tai yra, jei bandymas yra kokybės bandymas), pasirinkite matavimo vienetą, kuriuo turi būti įrašyti bandymo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="995c9-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="995c9-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="995c9-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="995c9-139">Išsaugoę bandymą, tinklelyje nebegalite **redaguoti** lauko Tipas.</span><span class="sxs-lookup"><span data-stu-id="995c9-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="995c9-140">Jei turite pakeisti tikrinimo rezultatų, kurie bus įrašyti patikrinti, tipą, veiksmų srityje **pasirinkite Keisti kokybės tikrinimo** tipą.</span><span class="sxs-lookup"><span data-stu-id="995c9-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="995c9-141">Dialogo lange Keisti kokybės tikrinimo tipą nustatykite norimą lauko Naujas tipas tipą ir **pasirinkite** **Gerai**, **kad** uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="995c9-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="995c9-142">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="995c9-142">Additional resources</span></span>

- [<span data-ttu-id="995c9-143">Kokybės valdymo bandymo instrumentai</span><span class="sxs-lookup"><span data-stu-id="995c9-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="995c9-144">Kokybės valdymo bandymo grupės</span><span class="sxs-lookup"><span data-stu-id="995c9-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="995c9-145">Kokybės valdymo bandymo kintamieji</span><span class="sxs-lookup"><span data-stu-id="995c9-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="995c9-146">Kokybės susiejimai</span><span class="sxs-lookup"><span data-stu-id="995c9-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
