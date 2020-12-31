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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684816"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="3d180-103">EMPTYRECORD ER funkcija</span><span class="sxs-lookup"><span data-stu-id="3d180-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d180-104">`EMPTYRECORD` funkcija grąžina nulinę *konteinerio (įrašo)* reikšmę, kurios struktūra yra tokia pati kaip nurodyto įrašų sąrašo arba įrašo.</span><span class="sxs-lookup"><span data-stu-id="3d180-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d180-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="3d180-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="3d180-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="3d180-106">Arguments</span></span>

<span data-ttu-id="3d180-107">`list`: *Įrašų sąrašas* arba *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="3d180-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="3d180-108">Tinkamas *Įrašų sąrašo* arba *Konteinerio (įrašo)* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="3d180-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3d180-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="3d180-109">Return values</span></span>

<span data-ttu-id="3d180-110">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="3d180-110">*Container (record)*</span></span>

<span data-ttu-id="3d180-111">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="3d180-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3d180-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="3d180-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="3d180-113">Neapibrėžtas įrašas yra toks, kurio visų laukų reikšmės yra tuščios.</span><span class="sxs-lookup"><span data-stu-id="3d180-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="3d180-114">Tuščia skaičių reikšmė yra **0** (nulis), eilučių – tuščia eilutė ir t. t.</span><span class="sxs-lookup"><span data-stu-id="3d180-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="3d180-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3d180-115">Example</span></span>

<span data-ttu-id="3d180-116">`EMPTYRECORD (SPLIT ("abc", 1))` grąžina naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį grąžina `SPLIT` funkcija.</span><span class="sxs-lookup"><span data-stu-id="3d180-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="3d180-117">Daugiau informacijos žr. [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="3d180-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d180-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3d180-118">Additional resources</span></span>

[<span data-ttu-id="3d180-119">Įrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="3d180-119">Record functions</span></span>](er-functions-category-record.md)
