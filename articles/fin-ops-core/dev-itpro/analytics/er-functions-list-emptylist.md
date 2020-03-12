---
title: ER EMPTYLIST funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) EMPTYLIST funkcija.
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
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042187"
---
# <span data-ttu-id="d20da-103"><a name="EMPTYLIST">ER EMPTYLIST funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d20da-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d20da-104">`EMPTYLIST` funkcija pateikia tuščią tipo *Įrašų sąrašas* reikšmę, kaip sąrašo struktūros šaltinį naudodama nurodytą sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d20da-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d20da-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="d20da-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="d20da-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d20da-106">Arguments</span></span>

<span data-ttu-id="d20da-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="d20da-107">`list`: *Record list*</span></span>

<span data-ttu-id="d20da-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="d20da-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d20da-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="d20da-109">Return values</span></span>

<span data-ttu-id="d20da-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="d20da-110">*Record list*</span></span>

<span data-ttu-id="d20da-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="d20da-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d20da-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d20da-112">Example</span></span>

<span data-ttu-id="d20da-113">`EMPTYLIST (SPLIT ("abc", 1))` pateikia naują tuščią sąrašą, kuris yra tokios pačios struktūros, kaip ir sąrašas, kurį pateikia naudojama `SPLIT` funkcija.</span><span class="sxs-lookup"><span data-stu-id="d20da-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d20da-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d20da-114">Additional resources</span></span>

[<span data-ttu-id="d20da-115">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="d20da-115">List functions</span></span>](er-functions-category-list.md)
