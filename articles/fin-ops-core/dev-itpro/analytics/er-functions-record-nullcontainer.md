---
title: NULLCONTAINER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NULLCONTAINER elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743932"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="96e3a-103">NULLCONTAINER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="96e3a-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96e3a-104">`NULLCONTAINER` funkcija grąžina nulinę *konteinerio (įrašo)* reikšmę, kurios struktūra yra tokia pati kaip nurodyto įrašų sąrašo arba įrašo.</span><span class="sxs-lookup"><span data-stu-id="96e3a-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e3a-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="96e3a-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="96e3a-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="96e3a-106">Arguments</span></span>

<span data-ttu-id="96e3a-107">`list`: *Įrašų sąrašas* arba *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="96e3a-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="96e3a-108">Tinkamas *Įrašų sąrašo* arba *Konteinerio (įrašo)* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="96e3a-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="96e3a-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="96e3a-109">Return values</span></span>

<span data-ttu-id="96e3a-110">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="96e3a-110">*Container (record)*</span></span>

<span data-ttu-id="96e3a-111">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="96e3a-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96e3a-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="96e3a-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="96e3a-113">Ši funkcija nebenaudojama.</span><span class="sxs-lookup"><span data-stu-id="96e3a-113">This function is obsolete.</span></span> <span data-ttu-id="96e3a-114">Naudokite `EMPTYRECORD` funkciją kaip pakaitą.</span><span class="sxs-lookup"><span data-stu-id="96e3a-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="96e3a-115">Daugiau informacijos žr. [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="96e3a-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="96e3a-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="96e3a-116">Example</span></span>

<span data-ttu-id="96e3a-117">`NULLCONTAINER (SPLIT ("abc", 1))` grąžina naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį grąžina `SPLIT` funkcija.</span><span class="sxs-lookup"><span data-stu-id="96e3a-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="96e3a-118">Daugiau informacijos žr. [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="96e3a-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96e3a-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="96e3a-119">Additional resources</span></span>

[<span data-ttu-id="96e3a-120">Įrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="96e3a-120">Record functions</span></span>](er-functions-category-record.md)
