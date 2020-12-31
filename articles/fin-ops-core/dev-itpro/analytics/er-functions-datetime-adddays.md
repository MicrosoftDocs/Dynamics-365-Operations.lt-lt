---
title: ER ADDDAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ADDDAYS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688448"
---
# <a name="adddays-er-function"></a><span data-ttu-id="57c98-103">ER ADDDAYS funkcija</span><span class="sxs-lookup"><span data-stu-id="57c98-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57c98-104">`ADDDAYS` funkcija apskaičiuoja *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.</span><span class="sxs-lookup"><span data-stu-id="57c98-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="57c98-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="57c98-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="57c98-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="57c98-106">Arguments</span></span>

<span data-ttu-id="57c98-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="57c98-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="57c98-108">Datos / laiko reikšmė, nurodanti pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="57c98-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="57c98-109">`days`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="57c98-109">`days`: *Integer*</span></span>

<span data-ttu-id="57c98-110">Dienų prieš `datetime` arba po jos skaičius.</span><span class="sxs-lookup"><span data-stu-id="57c98-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="57c98-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="57c98-111">Return values</span></span>

<span data-ttu-id="57c98-112">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="57c98-112">*DateTime*</span></span>

<span data-ttu-id="57c98-113">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="57c98-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="57c98-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="57c98-114">Usage notes</span></span>

<span data-ttu-id="57c98-115">Teigiama `days` reikšmė pateikia būsimą datą.</span><span class="sxs-lookup"><span data-stu-id="57c98-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="57c98-116">Neigiama reikšmė pateikia praeities datą.</span><span class="sxs-lookup"><span data-stu-id="57c98-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="57c98-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="57c98-117">Example 1</span></span>

<span data-ttu-id="57c98-118">`ADDDAYS (NOW(), 7)` nukelia datą ir laiką septyniomis dienomis į ateitį.</span><span class="sxs-lookup"><span data-stu-id="57c98-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="57c98-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="57c98-119">Example 2</span></span>

<span data-ttu-id="57c98-120">`ADDDAYS (NOW(), -3)` nukelia datą ir laiką trimis dienomis į praeitį.</span><span class="sxs-lookup"><span data-stu-id="57c98-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57c98-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="57c98-121">Additional resources</span></span>

[<span data-ttu-id="57c98-122">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="57c98-122">Date and time functions</span></span>](er-functions-category-datetime.md)
