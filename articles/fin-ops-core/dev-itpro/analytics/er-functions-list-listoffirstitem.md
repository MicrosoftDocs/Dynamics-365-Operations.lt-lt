---
title: ER LISTOFFIRSTITEM funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) LISTOFFIRSTITEM funkcija.
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
ms.openlocfilehash: 069ec0c6d5578ca6ab68814adf325bd79e73b9e8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745062"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="445c6-103">ER LISTOFFIRSTITEM funkcija</span><span class="sxs-lookup"><span data-stu-id="445c6-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="445c6-104">`LISTOFFIRSTITEM` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, kurią sudaro tik pirmasis nurodyto sąrašo įrašas.</span><span class="sxs-lookup"><span data-stu-id="445c6-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="445c6-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="445c6-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="445c6-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="445c6-106">Arguments</span></span>

<span data-ttu-id="445c6-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="445c6-107">`list`: *Record list*</span></span>

<span data-ttu-id="445c6-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="445c6-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="445c6-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="445c6-109">Return values</span></span>

<span data-ttu-id="445c6-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="445c6-110">*Record list*</span></span>

<span data-ttu-id="445c6-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="445c6-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="445c6-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="445c6-112">Example</span></span>

<span data-ttu-id="445c6-113">Reiškinys `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` pateikia teksto reikšmę **„A“**.</span><span class="sxs-lookup"><span data-stu-id="445c6-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="445c6-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="445c6-114">Additional resources</span></span>

[<span data-ttu-id="445c6-115">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="445c6-115">List functions</span></span>](er-functions-category-list.md)
