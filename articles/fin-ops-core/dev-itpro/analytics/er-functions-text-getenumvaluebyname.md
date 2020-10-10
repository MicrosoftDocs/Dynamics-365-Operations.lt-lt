---
title: GETENUMVALUEBYNAME ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GETENUMVALUEBYNAME elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885232"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="1f671-103">GETENUMVALUEBYNAME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="1f671-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f671-104">`GETENUMVALUEBYNAME`funkcija ieško nurodytame išvardijimo duomenų šaltinyje konkrečios *Enum* reikšmės, naudodama išvardijimo pavadinimą, kuris nurodytas kaip *Eilutės* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1f671-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="1f671-105">Jei *Enum* reikšmė randama, funkcija ją pateikia.</span><span class="sxs-lookup"><span data-stu-id="1f671-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="1f671-106">Priešingu atveju funkcija grąžina **null** išvardijimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f671-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f671-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1f671-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="1f671-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1f671-108">Arguments</span></span>

<span data-ttu-id="1f671-109">`enumeration data source path`: *Išvardijimas*</span><span class="sxs-lookup"><span data-stu-id="1f671-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="1f671-110">Tinkamas vieno iš tolesnių išvardijimo tipų duomenų šaltinio maršrutas:</span><span class="sxs-lookup"><span data-stu-id="1f671-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="1f671-111">Elektroninių ataskaitų (ER) modelių išvardijimas</span><span class="sxs-lookup"><span data-stu-id="1f671-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="1f671-112">ER formatų išvardijimas</span><span class="sxs-lookup"><span data-stu-id="1f671-112">ER format enumeration</span></span>
- <span data-ttu-id="1f671-113">„Microsoft Dynamics 365 Finance“ išvardijimas</span><span class="sxs-lookup"><span data-stu-id="1f671-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="1f671-114">`enumeration value text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1f671-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="1f671-115">Eilutės reikšmė, nurodanti vienos išvardijimo reikšmės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1f671-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f671-116">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="1f671-116">Return values</span></span>

<span data-ttu-id="1f671-117">*Išvard.* leidžiama reikšmė NULL</span><span class="sxs-lookup"><span data-stu-id="1f671-117">Nullable *Enum*</span></span>

<span data-ttu-id="1f671-118">Gaunama išvardijimo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1f671-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1f671-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="1f671-119">Usage notes</span></span>

<span data-ttu-id="1f671-120">Nėra pateikiama jokia išimtis, jei reikšmė *Enum* nerasta naudojant išvardijimo reikšmę, nurodytą kaip *Eilutės* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1f671-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="1f671-121">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1f671-121">Example 1</span></span>

<span data-ttu-id="1f671-122">Tolesnėje iliustracijoje duomenų modelyje įvestas išvardijimas **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="1f671-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="1f671-123">Atkreipkite dėmesį, kad išvardijimo reikšmėms nurodytos žymos.</span><span class="sxs-lookup"><span data-stu-id="1f671-123">Notice that labels are defined for the enumeration values.</span></span>

![Galimos duomenų modelio išvardijimo vertės](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="1f671-125">Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="1f671-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="1f671-126">Duomenų šaltinis **$Direction** sukonfigūruotas ER ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="1f671-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="1f671-127">Šis duomenų šaltinis yra sukonfigūruotas pagal modelių išvardijimą **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="1f671-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="1f671-128">Išraiška `$IsArrivals` sukurta naudoti modelių išvardijime veikiantį duomenų šaltinį **$Direction** kaip šios funkcijos parametrą.</span><span class="sxs-lookup"><span data-stu-id="1f671-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="1f671-129">Šios lyginamosios išraiškos reikšmė yra **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="1f671-129">The value of this comparison expression is **TRUE**.</span></span>

![Duomenų modelio išvardijimo pavyzdys](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="1f671-131">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1f671-131">Example 2</span></span>

<span data-ttu-id="1f671-132">`GETENUMVALUEBYNAME` ir [`LISTOFFIELDS`](er-functions-list-listoffields.md) funkcijos leidžia kaip teksto vertes iškviesti vertes ir palaikomų išvardijimų žymes.</span><span class="sxs-lookup"><span data-stu-id="1f671-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="1f671-133">(Palaikomi išvardijimai yra prašymų išvardijimai, duomenų modelio išvardijimai ir formato išvardijimai.)</span><span class="sxs-lookup"><span data-stu-id="1f671-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="1f671-134">Tolesnėje iliustracijoje **TransType** duomenų šaltinis pristatytas duomenų modelio susiejime.</span><span class="sxs-lookup"><span data-stu-id="1f671-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="1f671-135">Šis duomenų šaltinis nurodo **LedgerTransType** prašymo išvardijimą.</span><span class="sxs-lookup"><span data-stu-id="1f671-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Duomenų modelio susiejimo, kuris nurodo prašymo išvardijimą, duomenų šaltinis](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="1f671-137">Tolesnė iliustracija rodo **TransTypeList** duomenų šaltinį, konfigūruotą duomenų modelio susiejime.</span><span class="sxs-lookup"><span data-stu-id="1f671-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="1f671-138">Šis duomenų šaltinis yra sukonfigūruotas pagal **TransType** prašymo išvardijimą.</span><span class="sxs-lookup"><span data-stu-id="1f671-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="1f671-139">`LISTOFFIELDS` funkcija naudojama norint grąžinti visas išvardijimo vertes kaip įrašų, kuriuose yra laukų, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1f671-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="1f671-140">Tokiu būdu informacija apie kiekvieną išvardijimo vertę yra rodoma.</span><span class="sxs-lookup"><span data-stu-id="1f671-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="1f671-141">Laukas **EnumValue** yra sukonfigūruotas **TransTypeList** duomenų šaltiniui, naudojant `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` išraišką.</span><span class="sxs-lookup"><span data-stu-id="1f671-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="1f671-142">Šis laukas grąžina kiekvieno šio sąrašo įrašo išvardijimo vertę.</span><span class="sxs-lookup"><span data-stu-id="1f671-142">This field returns an enumeration value for every record in this list.</span></span>

![Duomenų modelio išdėstymo duomenų šaltinis, kuris grąžina visas pasirinkto išvardijimo vertes kaip įrašų sąrašą](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="1f671-144">Tolesnė iliustracija rodo **VendTrans** duomenų šaltinį, konfigūruotą duomenų modelio susiejime.</span><span class="sxs-lookup"><span data-stu-id="1f671-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="1f671-145">Šis duomenų šaltinis grąžina tiekėjo operacijų įrašus iš **VendTrans** programos lentelės.</span><span class="sxs-lookup"><span data-stu-id="1f671-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="1f671-146">Kiekvienos operacijos didžiosios knygos tipas apibrėžiamas **TransType** lauko verte.</span><span class="sxs-lookup"><span data-stu-id="1f671-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="1f671-147">Laukas **TransTypeTitle** yra sukonfigūruotas **VendTrans** duomenų šaltiniui, naudojant `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` išraišką.</span><span class="sxs-lookup"><span data-stu-id="1f671-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="1f671-148">Šis laukas grąžina esamos operacijos, kaip teksto, išvardijimo vertės žymę, jei ši išvardijimo vertė yra galima.</span><span class="sxs-lookup"><span data-stu-id="1f671-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="1f671-149">Kitu atveju, jis pateikia tuščią eilutės vertę.</span><span class="sxs-lookup"><span data-stu-id="1f671-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="1f671-150">Laukas **TransTypeTitle** yra susietas su duomenų modelio, kuris įgalina šią informaciją naudoti kiekvienu ER formatu, kuris naudoja duomenų modelį kaip duomenų šaltinį, **LedgerType** lauku.</span><span class="sxs-lookup"><span data-stu-id="1f671-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Duomenų modelio susiejimo, kuris grąžina tiekėjo operacijas, duomenų šaltinis](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="1f671-152">Toliau pateiktoje iliustracijoje parodyta, kaip galite naudoti [duomenų šaltinio derintuvę](er-debug-data-sources.md), kad galėtumėte patikrinti sukonfigūruotą duomenų modelio susiejimą.</span><span class="sxs-lookup"><span data-stu-id="1f671-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Duomenų šaltinio derintuvės naudojimas, norint patikrinti sukonfigūruotą duomenų modelio susiejimą](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="1f671-154">**LedgerType** duomenų modelio laukas rodo operacijų tipų žymas numatytu būdu.</span><span class="sxs-lookup"><span data-stu-id="1f671-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="1f671-155">Jei planuojate naudoti šį metodą dideliam operacijų duomenų kiekiui, turite apsvarstyti vykdymo efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="1f671-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="1f671-156">Daugiau informacijos, žr. [ER formatų vykdymo sekimas, siekiant pašalinti našumo problemas](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="1f671-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f671-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1f671-157">Additional resources</span></span>

[<span data-ttu-id="1f671-158">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="1f671-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="1f671-159">ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas</span><span class="sxs-lookup"><span data-stu-id="1f671-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="1f671-160">ER LISTOFFIELDS funkcija</span><span class="sxs-lookup"><span data-stu-id="1f671-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="1f671-161">ER FIRSTORNULL funkcija</span><span class="sxs-lookup"><span data-stu-id="1f671-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="1f671-162">WHERE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="1f671-162">WHERE ER function</span></span>](er-functions-list-where.md)
