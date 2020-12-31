---
title: ER LISTOFFIELDS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) LISTOFFIELDS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8d9f41d6ee5256f560c83486c95ecd47f5b081
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686517"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="86728-103">ER LISTOFFIELDS funkcija</span><span class="sxs-lookup"><span data-stu-id="86728-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86728-104">`LISTOFFIELDS` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal nurodyto tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą.</span><span class="sxs-lookup"><span data-stu-id="86728-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="86728-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="86728-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="86728-106">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="86728-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="86728-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="86728-107">Arguments</span></span>

<span data-ttu-id="86728-108">`path`: Duomenų šaltinio nuroda</span><span class="sxs-lookup"><span data-stu-id="86728-108">`path`: Data source reference</span></span>

<span data-ttu-id="86728-109">Tinkamas vieno iš tolesnių duomenų tipų duomenų šaltinio nuorodos kelias.</span><span class="sxs-lookup"><span data-stu-id="86728-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="86728-110">Modelių išvardijimas</span><span class="sxs-lookup"><span data-stu-id="86728-110">Model enumeration</span></span>
- <span data-ttu-id="86728-111">Formatų išvardijimas</span><span class="sxs-lookup"><span data-stu-id="86728-111">Format enumeration</span></span>
- <span data-ttu-id="86728-112">Programų išvardijimas</span><span class="sxs-lookup"><span data-stu-id="86728-112">Application enumeration</span></span>
- <span data-ttu-id="86728-113">Konteineris (įrašas)</span><span class="sxs-lookup"><span data-stu-id="86728-113">Container (record)</span></span>

<span data-ttu-id="86728-114">`language`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="86728-114">`language`: *String*</span></span>

<span data-ttu-id="86728-115">Tekstas, reiškiantis kalbos kodą.</span><span class="sxs-lookup"><span data-stu-id="86728-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="86728-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="86728-116">Return values</span></span>

<span data-ttu-id="86728-117">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="86728-117">*Record list*</span></span>

<span data-ttu-id="86728-118">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="86728-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="86728-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="86728-119">Usage notes</span></span>

<span data-ttu-id="86728-120">Sukurtą sąrašą sudaro įrašai su tolesniais laukais.</span><span class="sxs-lookup"><span data-stu-id="86728-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="86728-121">**Pavadinimas** (duomenų tipas *Eilutė*)</span><span class="sxs-lookup"><span data-stu-id="86728-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="86728-122">**Žyma** (duomenų tipas *Eilutė*)</span><span class="sxs-lookup"><span data-stu-id="86728-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="86728-123">**Aprašas** (duomenų tipas *Eilutė*)</span><span class="sxs-lookup"><span data-stu-id="86728-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="86728-124">**IsTranslated** (duomenų tipas *Bulio logika*)</span><span class="sxs-lookup"><span data-stu-id="86728-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="86728-125">Jei `path` argumentas nurodo tipo *Konteineris (įrašas)* duomenų šaltinį, kiekviename nurodyto konteinerio įrašo lauke į sukurtą sąrašą įtraukiamas naujas įrašas.</span><span class="sxs-lookup"><span data-stu-id="86728-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="86728-126">Kiekvieno sukurto įrašo laukas **Pavadinimas** pateikia nurodyto konteinerio įrašo, kuriam buvo sukurtas dabartinis įrašas, lauko pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="86728-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="86728-127">Jei `path` argumentas nurodo vieno iš tipų *Išvardijimas* duomenų šaltinį, kiekvienos nurodyto išvardijimo reikšmės atveju į sukurtą sąrašą įtraukiamas naujas įrašas.</span><span class="sxs-lookup"><span data-stu-id="86728-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="86728-128">Kiekvieno sukurto įrašo laukas **Pavadinimas** pateikia nurodyto išvardijimo, kuriam buvo sukurtas dabartinis įrašas, reikšmę, laukas **Aprašas** pateikia to išvardijimo aprašą, o laukas **Žyma** – to išvardijimo žymą.</span><span class="sxs-lookup"><span data-stu-id="86728-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="86728-129">Kai vykdant naudojama 1-oji sintaksė, laukuose **Žyma** ir **Aprašas** turi būti pateikiamos reikšmės, paremtos vykdomo modulio Elektroninės ataskaitų (ER) formato kalbos parametrais.</span><span class="sxs-lookup"><span data-stu-id="86728-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="86728-130">Jei pageidaujamos kalbos žymos ir aprašai yra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos ta kalba, o lauke **IsTranslated** pateikiama **True**.</span><span class="sxs-lookup"><span data-stu-id="86728-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="86728-131">Jei pageidaujamos kalbos žymos ir aprašai nėra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos numatytąja kalba **EN-US**, o lauke **IsTranslated** pateikiama **False**.</span><span class="sxs-lookup"><span data-stu-id="86728-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="86728-132">Kai vykdant naudojama 2-oji sintaksė, laukuose **Žyma** ir **Aprašas** turi būti pateikiamos reikšmės, paremtos kalba, kuri apibrėžta kaip antrasis iškviestos funkcijos argumentas.</span><span class="sxs-lookup"><span data-stu-id="86728-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="86728-133">Jei pageidaujamos kalbos žymos ir aprašai yra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos ta kalba, o lauke **IsTranslated** pateikiama **True**.</span><span class="sxs-lookup"><span data-stu-id="86728-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="86728-134">Jei pageidaujamos kalbos žymos ir aprašai nėra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos kalba **EN-US**, o lauke **IsTranslated** pateikiama **False**.</span><span class="sxs-lookup"><span data-stu-id="86728-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="86728-135">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="86728-135">Example 1</span></span>

<span data-ttu-id="86728-136">Tolesnėje iliustracijoje ER duomenų modelyje įvestas išvardijimas.</span><span class="sxs-lookup"><span data-stu-id="86728-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="86728-137">Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="86728-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="86728-138">Modelio išvardijimas įtrauktas į ataskaitą kaip duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="86728-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="86728-139">ER reiškinyje modelio išvardijimas naudojamas kaip funkcijos `LISTOFFIELDS` parametras.</span><span class="sxs-lookup"><span data-stu-id="86728-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="86728-140">Tipo *Įrašų sąrašas* duomenų šaltinis įterpiamas į ataskaitą naudojant sukurtą ER reiškinį.</span><span class="sxs-lookup"><span data-stu-id="86728-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="86728-141">Toliau pateiktame pavyzdyje parodyti ER formato elementai, susieti su tipo *Įrašų sąrašas* duomenų šaltiniu, kuris buvo sukurtas naudojant funkciją `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="86728-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="86728-142">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</span><span class="sxs-lookup"><span data-stu-id="86728-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="86728-143">Pagal pirminių formato elementų **FAILAS** ir **APLANKAS** kalbos parametrus išverstas žymų ir aprašų tekstas yra įvedamas į ER formato išeigą.</span><span class="sxs-lookup"><span data-stu-id="86728-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="86728-144">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="86728-144">Example 2</span></span>

<span data-ttu-id="86728-145">Duomenų šaltinio tipas *Apskaičiuotasis laukas* naudojamas norint konfigūruoti **enumType** duomenų modelio išvardijimo duomenų šaltinius **enumType\_de** ir **enumType\_deCH**.</span><span class="sxs-lookup"><span data-stu-id="86728-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="86728-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="86728-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="86728-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="86728-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="86728-148">Tokiu atveju naudodami tolesnį reiškinį galite gauti išvardijimo reikšmės žymą Šveicarijos vokiečių kalba (jei toks vertimas yra).</span><span class="sxs-lookup"><span data-stu-id="86728-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="86728-149">Jei vertimas Šveicarijos vokiečių kalba nepateikiamas, žyma pateikiama vokiečių kalba.</span><span class="sxs-lookup"><span data-stu-id="86728-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="86728-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="86728-150">Additional resources</span></span>

[<span data-ttu-id="86728-151">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="86728-151">List functions</span></span>](er-functions-category-list.md)
