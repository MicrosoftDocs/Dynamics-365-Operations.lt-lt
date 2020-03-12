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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042003"
---
# <span data-ttu-id="7c7d8-103"><a name="LISTOFFIELDS">ER LISTOFFIELDS funkcija</a></span><span class="sxs-lookup"><span data-stu-id="7c7d8-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c7d8-104">`LISTOFFIELDS` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal nurodyto tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="7c7d8-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="7c7d8-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="7c7d8-106">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="7c7d8-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="7c7d8-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="7c7d8-107">Arguments</span></span>

<span data-ttu-id="7c7d8-108">`path`: Duomenų šaltinio nuroda</span><span class="sxs-lookup"><span data-stu-id="7c7d8-108">`path`: Data source reference</span></span>

<span data-ttu-id="7c7d8-109">Tinkamas vieno iš tolesnių duomenų tipų duomenų šaltinio nuorodos kelias.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="7c7d8-110">Modelių išvardijimas</span><span class="sxs-lookup"><span data-stu-id="7c7d8-110">Model enumeration</span></span>
- <span data-ttu-id="7c7d8-111">Formatų išvardijimas</span><span class="sxs-lookup"><span data-stu-id="7c7d8-111">Format enumeration</span></span>
- <span data-ttu-id="7c7d8-112">Programų išvardijimas</span><span class="sxs-lookup"><span data-stu-id="7c7d8-112">Application enumeration</span></span>
- <span data-ttu-id="7c7d8-113">Konteineris (įrašas)</span><span class="sxs-lookup"><span data-stu-id="7c7d8-113">Container (record)</span></span>

<span data-ttu-id="7c7d8-114">`language`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="7c7d8-114">`language`: *String*</span></span>

<span data-ttu-id="7c7d8-115">Tekstas, reiškiantis kalbos kodą.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c7d8-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="7c7d8-116">Return values</span></span>

<span data-ttu-id="7c7d8-117">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="7c7d8-117">*Record list*</span></span>

<span data-ttu-id="7c7d8-118">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7c7d8-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="7c7d8-119">Usage notes</span></span>

<span data-ttu-id="7c7d8-120">Sukurtą sąrašą sudaro įrašai su tolesniais laukais.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="7c7d8-121">**Pavadinimas** (duomenų tipas *Eilutė*)</span><span class="sxs-lookup"><span data-stu-id="7c7d8-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="7c7d8-122">**Žyma** (duomenų tipas *Eilutė*)</span><span class="sxs-lookup"><span data-stu-id="7c7d8-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="7c7d8-123">**Aprašas** (duomenų tipas *Eilutė*)</span><span class="sxs-lookup"><span data-stu-id="7c7d8-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="7c7d8-124">**IsTranslated** (duomenų tipas *Bulio logika*)</span><span class="sxs-lookup"><span data-stu-id="7c7d8-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="7c7d8-125">Jei `path` argumentas nurodo tipo *Konteineris (įrašas)* duomenų šaltinį, kiekviename nurodyto konteinerio įrašo lauke į sukurtą sąrašą įtraukiamas naujas įrašas.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="7c7d8-126">Kiekvieno sukurto įrašo laukas **Pavadinimas** pateikia nurodyto konteinerio įrašo, kuriam buvo sukurtas dabartinis įrašas, lauko pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="7c7d8-127">Jei `path` argumentas nurodo vieno iš tipų *Išvardijimas* duomenų šaltinį, kiekvienos nurodyto išvardijimo reikšmės atveju į sukurtą sąrašą įtraukiamas naujas įrašas.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="7c7d8-128">Kiekvieno sukurto įrašo laukas **Pavadinimas** pateikia nurodyto išvardijimo, kuriam buvo sukurtas dabartinis įrašas, reikšmę, laukas **Aprašas** pateikia to išvardijimo aprašą, o laukas **Žyma** – to išvardijimo žymą.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="7c7d8-129">Kai vykdant naudojama 1-oji sintaksė, laukuose **Žyma** ir **Aprašas** turi būti pateikiamos reikšmės, paremtos vykdomo modulio Elektroninės ataskaitų (ER) formato kalbos parametrais.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="7c7d8-130">Jei pageidaujamos kalbos žymos ir aprašai yra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos ta kalba, o lauke **IsTranslated** pateikiama **True**.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="7c7d8-131">Jei pageidaujamos kalbos žymos ir aprašai nėra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos numatytąja kalba **EN-US**, o lauke **IsTranslated** pateikiama **False**.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="7c7d8-132">Kai vykdant naudojama 2-oji sintaksė, laukuose **Žyma** ir **Aprašas** turi būti pateikiamos reikšmės, paremtos kalba, kuri apibrėžta kaip antrasis iškviestos funkcijos argumentas.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="7c7d8-133">Jei pageidaujamos kalbos žymos ir aprašai yra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos ta kalba, o lauke **IsTranslated** pateikiama **True**.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="7c7d8-134">Jei pageidaujamos kalbos žymos ir aprašai nėra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos kalba **EN-US**, o lauke **IsTranslated** pateikiama **False**.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="7c7d8-135">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7c7d8-135">Example 1</span></span>

<span data-ttu-id="7c7d8-136">Tolesnėje iliustracijoje ER duomenų modelyje įvestas išvardijimas.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="7c7d8-137">Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="7c7d8-138">Modelio išvardijimas įtrauktas į ataskaitą kaip duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="7c7d8-139">ER reiškinyje modelio išvardijimas naudojamas kaip funkcijos `LISTOFFIELDS` parametras.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="7c7d8-140">Tipo *Įrašų sąrašas* duomenų šaltinis įterpiamas į ataskaitą naudojant sukurtą ER reiškinį.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="7c7d8-141">Toliau pateiktame pavyzdyje parodyti ER formato elementai, susieti su tipo *Įrašų sąrašas* duomenų šaltiniu, kuris buvo sukurtas naudojant funkciją `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="7c7d8-142">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="7c7d8-143">Pagal pirminių formato elementų **FAILAS** ir **APLANKAS** kalbos parametrus išverstas žymų ir aprašų tekstas yra įvedamas į ER formato išeigą.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="7c7d8-144">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7c7d8-144">Example 2</span></span>

<span data-ttu-id="7c7d8-145">Duomenų šaltinio tipas *Apskaičiuotasis laukas* naudojamas norint konfigūruoti **enumType** duomenų modelio išvardijimo duomenų šaltinius **enumType\_de** ir **enumType\_deCH**.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="7c7d8-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="7c7d8-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="7c7d8-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="7c7d8-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="7c7d8-148">Tokiu atveju naudodami tolesnį reiškinį galite gauti išvardijimo reikšmės žymą Šveicarijos vokiečių kalba (jei toks vertimas yra).</span><span class="sxs-lookup"><span data-stu-id="7c7d8-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="7c7d8-149">Jei vertimas Šveicarijos vokiečių kalba nepateikiamas, žyma pateikiama vokiečių kalba.</span><span class="sxs-lookup"><span data-stu-id="7c7d8-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="7c7d8-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7c7d8-150">Additional resources</span></span>

[<span data-ttu-id="7c7d8-151">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="7c7d8-151">List functions</span></span>](er-functions-category-list.md)
