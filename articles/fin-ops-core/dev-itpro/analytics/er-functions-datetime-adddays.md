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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08b9727fb34210fecff31826cc1f2b8da022156b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042463"
---
# <span data-ttu-id="aa268-103"><a name="ADDDAYS">ER ADDDAYS funkcija</a></span><span class="sxs-lookup"><span data-stu-id="aa268-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa268-104">`ADDDAYS` funkcija apskaičiuoja *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.</span><span class="sxs-lookup"><span data-stu-id="aa268-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa268-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="aa268-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="aa268-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="aa268-106">Arguments</span></span>

<span data-ttu-id="aa268-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="aa268-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="aa268-108">Datos / laiko reikšmė, nurodanti pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="aa268-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="aa268-109">`days`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="aa268-109">`days`: *Integer*</span></span>

<span data-ttu-id="aa268-110">Dienų prieš `datetime` arba po jos skaičius.</span><span class="sxs-lookup"><span data-stu-id="aa268-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="aa268-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="aa268-111">Return values</span></span>

<span data-ttu-id="aa268-112">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="aa268-112">*DateTime*</span></span>

<span data-ttu-id="aa268-113">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="aa268-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aa268-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="aa268-114">Usage notes</span></span>

<span data-ttu-id="aa268-115">Teigiama `days` reikšmė pateikia būsimą datą.</span><span class="sxs-lookup"><span data-stu-id="aa268-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="aa268-116">Neigiama reikšmė pateikia praeities datą.</span><span class="sxs-lookup"><span data-stu-id="aa268-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="aa268-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="aa268-117">Example 1</span></span>

<span data-ttu-id="aa268-118">`ADDDAYS (NOW(), 7)` nukelia datą ir laiką septyniomis dienomis į ateitį.</span><span class="sxs-lookup"><span data-stu-id="aa268-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="aa268-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="aa268-119">Example 2</span></span>

<span data-ttu-id="aa268-120">`ADDDAYS (NOW(), -3)` nukelia datą ir laiką trimis dienomis į praeitį.</span><span class="sxs-lookup"><span data-stu-id="aa268-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa268-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="aa268-121">Additional resources</span></span>

[<span data-ttu-id="aa268-122">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="aa268-122">Date and time functions</span></span>](er-functions-category-datetime.md)
