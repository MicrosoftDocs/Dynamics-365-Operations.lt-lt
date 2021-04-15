---
title: ER ADDDAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ADDDAYS funkcija.
author: NickSelin
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747064"
---
# <a name="adddays-er-function"></a><span data-ttu-id="07179-103">ER ADDDAYS funkcija</span><span class="sxs-lookup"><span data-stu-id="07179-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07179-104">`ADDDAYS` funkcija apskaičiuoja *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.</span><span class="sxs-lookup"><span data-stu-id="07179-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="07179-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="07179-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="07179-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="07179-106">Arguments</span></span>

<span data-ttu-id="07179-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="07179-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="07179-108">Datos / laiko reikšmė, nurodanti pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="07179-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="07179-109">`days`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="07179-109">`days`: *Integer*</span></span>

<span data-ttu-id="07179-110">Dienų prieš `datetime` arba po jos skaičius.</span><span class="sxs-lookup"><span data-stu-id="07179-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="07179-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="07179-111">Return values</span></span>

<span data-ttu-id="07179-112">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="07179-112">*DateTime*</span></span>

<span data-ttu-id="07179-113">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="07179-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="07179-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="07179-114">Usage notes</span></span>

<span data-ttu-id="07179-115">Teigiama `days` reikšmė pateikia būsimą datą.</span><span class="sxs-lookup"><span data-stu-id="07179-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="07179-116">Neigiama reikšmė pateikia praeities datą.</span><span class="sxs-lookup"><span data-stu-id="07179-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="07179-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="07179-117">Example 1</span></span>

<span data-ttu-id="07179-118">`ADDDAYS (NOW(), 7)` nukelia datą ir laiką septyniomis dienomis į ateitį.</span><span class="sxs-lookup"><span data-stu-id="07179-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="07179-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="07179-119">Example 2</span></span>

<span data-ttu-id="07179-120">`ADDDAYS (NOW(), -3)` nukelia datą ir laiką trimis dienomis į praeitį.</span><span class="sxs-lookup"><span data-stu-id="07179-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07179-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="07179-121">Additional resources</span></span>

[<span data-ttu-id="07179-122">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="07179-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]