---
title: ER DAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916297"
---
# <span data-ttu-id="81dcc-103"><a name="DAYS">DAYS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="81dcc-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81dcc-104">`DAYS` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="81dcc-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dcc-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="81dcc-105">Syntax</span></span>

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="81dcc-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="81dcc-106">Arguments</span></span>

<span data-ttu-id="81dcc-107">`date 1`: *Data*</span><span class="sxs-lookup"><span data-stu-id="81dcc-107">`date 1`: *Date*</span></span>

<span data-ttu-id="81dcc-108">Datos reikšmė, nurodanti pradžios datą dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="81dcc-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="81dcc-109">`date 2`: *Data*</span><span class="sxs-lookup"><span data-stu-id="81dcc-109">`date 2`: *Date*</span></span>

<span data-ttu-id="81dcc-110">Datos reikšmė, nurodanti pabaigos datą dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="81dcc-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="81dcc-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="81dcc-111">Return values</span></span>

<span data-ttu-id="81dcc-112">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="81dcc-112">*Integer*</span></span>

<span data-ttu-id="81dcc-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="81dcc-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81dcc-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="81dcc-114">Usage notes</span></span>

<span data-ttu-id="81dcc-115">Kai pirmoji data yra vėlesnė nei antroji, `DAYS` funkcija pateikia teigiamą reikšmę, kai pirmoji data sutampa su antrąja, ji pateikia **0** (nulį), o, kai pirmoji data yra ankstesnė nei antroji data, ji pateikia neigiamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="81dcc-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="81dcc-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="81dcc-116">Example</span></span>

<span data-ttu-id="81dcc-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` pateikia **–1**.</span><span class="sxs-lookup"><span data-stu-id="81dcc-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81dcc-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="81dcc-118">Additional resources</span></span>

[<span data-ttu-id="81dcc-119">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="81dcc-119">Date and time functions</span></span>](er-functions-category-datetime.md)
