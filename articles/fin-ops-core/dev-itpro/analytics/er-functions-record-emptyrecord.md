---
title: EMPTYRECORD ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama EMPTYRECORD elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: a02cdd085a236065bb3622b36f7d3284144d96e5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041290"
---
# <span data-ttu-id="4108e-103"><a name="EMPTYRECORD">EMPTYRECORD ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="4108e-103"><a name="EMPTYRECORD">EMPTYRECORD ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4108e-104">`EMPTYRECORD` funkcija grąžina nulinę *konteinerio (įrašo)* reikšmę, kurios struktūra yra tokia pati kaip nurodyto įrašų sąrašo arba įrašo.</span><span class="sxs-lookup"><span data-stu-id="4108e-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4108e-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="4108e-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="4108e-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="4108e-106">Arguments</span></span>

<span data-ttu-id="4108e-107">`list`: *Įrašų sąrašas* arba *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="4108e-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="4108e-108">Tinkamas *Įrašų sąrašo* arba *Konteinerio (įrašo)* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="4108e-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4108e-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="4108e-109">Return values</span></span>

<span data-ttu-id="4108e-110">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="4108e-110">*Container (record)*</span></span>

<span data-ttu-id="4108e-111">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4108e-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4108e-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="4108e-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="4108e-113">Neapibrėžtas įrašas yra toks, kurio visų laukų reikšmės yra tuščios.</span><span class="sxs-lookup"><span data-stu-id="4108e-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="4108e-114">Tuščia skaičių reikšmė yra **0** (nulis), eilučių – tuščia eilutė ir t. t.</span><span class="sxs-lookup"><span data-stu-id="4108e-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="4108e-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4108e-115">Example</span></span>

<span data-ttu-id="4108e-116">`EMPTYRECORD (SPLIT ("abc", 1))` grąžina naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį grąžina `SPLIT` funkcija.</span><span class="sxs-lookup"><span data-stu-id="4108e-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="4108e-117">Daugiau informacijos žr. [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="4108e-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4108e-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4108e-118">Additional resources</span></span>

[<span data-ttu-id="4108e-119">Įrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="4108e-119">Record functions</span></span>](er-functions-category-record.md)
