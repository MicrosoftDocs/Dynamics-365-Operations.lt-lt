---
title: JSONVALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama JSONVALUE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041235"
---
# <span data-ttu-id="17fda-103"><a name="JSONVALUE">JSONVALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="17fda-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17fda-104">`JSONVALUE` funkcija analizuojami duomenys „JavaScript Object Notation“ (JSON) formatu, kuris pasiekiamas nurodytu keliu bei norint išskleisti skaliarinę vertę, turinčią nurodytą ID.</span><span class="sxs-lookup"><span data-stu-id="17fda-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="17fda-105">Tada grąžinama išskleista skaliarinė reikšmė kaip *Eilutės* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="17fda-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fda-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="17fda-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="17fda-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="17fda-107">Arguments</span></span>

<span data-ttu-id="17fda-108">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="17fda-108">`input`: *String*</span></span>

<span data-ttu-id="17fda-109">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas, kuriame yra JSON duomenų.</span><span class="sxs-lookup"><span data-stu-id="17fda-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="17fda-110">`path`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="17fda-110">`path`: *String*</span></span>

<span data-ttu-id="17fda-111">Skaliarinės reikšmės JSON duomenų identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="17fda-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="17fda-112">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="17fda-112">Return values</span></span>

<span data-ttu-id="17fda-113">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="17fda-113">*String*</span></span>

<span data-ttu-id="17fda-114">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="17fda-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="17fda-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="17fda-115">Example</span></span>

<span data-ttu-id="17fda-116">Duomenų šaltinyje **JsonField** yra toliau nurodyti duomenys JSON formatu: **{„BuildNumber“:„7.3.1234.1“, „KeyThumbprint“:„7366E“}**.</span><span class="sxs-lookup"><span data-stu-id="17fda-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="17fda-117">Tokiu atveju išraiška `JSONVALUE (JsonField, "BuildNumber")` grąžina šią *Eilutės* duomenų tipo reikšmę: **„7.3.1234.1“**.</span><span class="sxs-lookup"><span data-stu-id="17fda-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17fda-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="17fda-118">Additional resources</span></span>

[<span data-ttu-id="17fda-119">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="17fda-119">Text functions</span></span>](er-functions-category-text.md)
