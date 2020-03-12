---
title: FORMAT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FORMAT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 7ae688ef6b24f8d90c0354c8c6449adba1588bfa
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041083"
---
# <span data-ttu-id="217e8-103"><a name="FORMAT">FORMAT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="217e8-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="217e8-104">`FORMAT` funkcija grąžina nurodytą eilutę kaip *Eilutės* reikšmę, suformatuotą pakeičiant visus **%N** pasikartojimus *N*-uoju argumentu.</span><span class="sxs-lookup"><span data-stu-id="217e8-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="217e8-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="217e8-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="217e8-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="217e8-106">Arguments</span></span>

<span data-ttu-id="217e8-107">`string`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="217e8-107">`string`: *String*</span></span>

<span data-ttu-id="217e8-108">Nuoroda į duomenų šaltinį, kuris yra formatuotinas *Eilutės* tipas.</span><span class="sxs-lookup"><span data-stu-id="217e8-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="217e8-109">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="217e8-109">This argument is required.</span></span>

<span data-ttu-id="217e8-110">`argument 1`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="217e8-110">`argument 1`: *String*</span></span>

<span data-ttu-id="217e8-111">Pirmasis argumentas, kuris yra naudojamas pakeisti **%1** pasikartojimus.</span><span class="sxs-lookup"><span data-stu-id="217e8-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="217e8-112">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="217e8-112">This argument is required.</span></span>

<span data-ttu-id="217e8-113">`argument N`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="217e8-113">`argument N`: *String*</span></span>

<span data-ttu-id="217e8-114">*N*-tasis argumentas, kuris yra naudojamas pakeisti **%2**, **%3** ir kitus pasikartojimus.</span><span class="sxs-lookup"><span data-stu-id="217e8-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="217e8-115">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="217e8-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="217e8-116">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="217e8-116">Return values</span></span>

<span data-ttu-id="217e8-117">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="217e8-117">*String*</span></span>

<span data-ttu-id="217e8-118">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="217e8-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="217e8-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="217e8-119">Usage notes</span></span>

<span data-ttu-id="217e8-120">Jei nėra pateiktas parametro argumentas, parametras eilutėje pateikiamas kaip **„%N“**.</span><span class="sxs-lookup"><span data-stu-id="217e8-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="217e8-121">*Realiojo skaičiaus* tipo reikšmių numatytosios eilutės konvertavimas apribotas dviem skaičiais po kablelio.</span><span class="sxs-lookup"><span data-stu-id="217e8-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="217e8-122">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="217e8-122">Example</span></span>

<span data-ttu-id="217e8-123">Tolesnėje iliustracijoje duomenų šaltinis **PaymentModel** grąžina klientų įrašų sąrašą naudodamas **kliento** komponentą.</span><span class="sxs-lookup"><span data-stu-id="217e8-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="217e8-124">Jis grąžina apdorojimo datos reikšmę naudojant lauką **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="217e8-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="217e8-125">Elektroninių ataskaitų (ER) formate, skirtame generuoti elektroninį failą pasirinktiems klientams, **PaymentModel** yra pasirinktas kaip duomenų šaltinis ir jis kontroliuoja proceso eigą.</span><span class="sxs-lookup"><span data-stu-id="217e8-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="217e8-126">Pateikiama išimtis, informuojanti vartotoją, jei pasirinktas klientas sustabdomas ataskaitos apdorojimo dieną.</span><span class="sxs-lookup"><span data-stu-id="217e8-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="217e8-127">Formulė, sukurta šio tipo apdorojimo kontrolei, gali naudoti tokius išteklius:</span><span class="sxs-lookup"><span data-stu-id="217e8-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="217e8-128">Žymė SYS70894, kur nurodytas toks tekstas:</span><span class="sxs-lookup"><span data-stu-id="217e8-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="217e8-129">**LT kalba:** „Nėra ką spausdinti“</span><span class="sxs-lookup"><span data-stu-id="217e8-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="217e8-130">**DE kalba:** „Nichts zu drucken“</span><span class="sxs-lookup"><span data-stu-id="217e8-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="217e8-131">Žymė SYS18389, kur nurodytas toks tekstas:</span><span class="sxs-lookup"><span data-stu-id="217e8-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="217e8-132">**EN-US kalba:** „Customer %1 is stopped for %2.“</span><span class="sxs-lookup"><span data-stu-id="217e8-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="217e8-133">**DE kalba:** „Debitor '%1' wird für %2 gesperrt.“</span><span class="sxs-lookup"><span data-stu-id="217e8-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="217e8-134">Tai yra išraiška, kurią galima sukurti.</span><span class="sxs-lookup"><span data-stu-id="217e8-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="217e8-135">Jei 2015 m. gruodžio 17 d. apdorojama kliento **Litware Retail** kultūros **EN-US** ir kalbos **EN-US** ataskaita, ši formulė pateikia tokį tekstą, kuris vartotojui gali būti pateiktas kaip tolesnis išimties pranešimas.</span><span class="sxs-lookup"><span data-stu-id="217e8-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="217e8-136">*Nėra spausdinių. „Customer Litware Retail“ sustabdytas 2015-12-17.*</span><span class="sxs-lookup"><span data-stu-id="217e8-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="217e8-137">Jei ta pati ataskaita apdorojama **„Litware Retail“** klientui 2015 m. gruodžio 17 d. pagal **DE** kultūrą ir **DE** kalbą, ši formulė pateikia tokį tekstą, kuris naudoja toliau nurodytą kitokį datos formatą.</span><span class="sxs-lookup"><span data-stu-id="217e8-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="217e8-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="217e8-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="217e8-139">ER formulėse žymoms taikoma tokia sintaksė:</span><span class="sxs-lookup"><span data-stu-id="217e8-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="217e8-140">**„Microsoft Dynamics 365 Finance“ programos išteklių žymėms:** **\@X**, kai **X** yra žymės ID programos objektų medyje (AOT)</span><span class="sxs-lookup"><span data-stu-id="217e8-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="217e8-141">**ER konfigūracijose esančioms žymėms:** **@"GER_LABEL:X"**, kai **X** yra žymės ID ER konfigūracijoje</span><span class="sxs-lookup"><span data-stu-id="217e8-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="217e8-142">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="217e8-142">Additional resources</span></span>

[<span data-ttu-id="217e8-143">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="217e8-143">Text functions</span></span>](er-functions-category-text.md)
