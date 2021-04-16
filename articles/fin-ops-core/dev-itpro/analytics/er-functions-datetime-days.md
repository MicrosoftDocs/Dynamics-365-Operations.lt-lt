---
title: ER DAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYS funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746896"
---
# <a name="days-er-function"></a><span data-ttu-id="dbb45-103">ER DAYS funkcija</span><span class="sxs-lookup"><span data-stu-id="dbb45-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbb45-104">`DAYS` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="dbb45-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb45-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="dbb45-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="dbb45-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="dbb45-106">Arguments</span></span>

<span data-ttu-id="dbb45-107">`date 1`: *Data*</span><span class="sxs-lookup"><span data-stu-id="dbb45-107">`date 1`: *Date*</span></span>

<span data-ttu-id="dbb45-108">Datos reikšmė, nurodanti pradžios datą dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="dbb45-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="dbb45-109">`date 2`: *Data*</span><span class="sxs-lookup"><span data-stu-id="dbb45-109">`date 2`: *Date*</span></span>

<span data-ttu-id="dbb45-110">Datos reikšmė, nurodanti pabaigos datą dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="dbb45-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="dbb45-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="dbb45-111">Return values</span></span>

<span data-ttu-id="dbb45-112">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="dbb45-112">*Integer*</span></span>

<span data-ttu-id="dbb45-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="dbb45-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dbb45-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="dbb45-114">Usage notes</span></span>

<span data-ttu-id="dbb45-115">Kai pirmoji data yra vėlesnė nei antroji, `DAYS` funkcija pateikia teigiamą reikšmę, kai pirmoji data sutampa su antrąja, ji pateikia **0** (nulį), o, kai pirmoji data yra ankstesnė nei antroji data, ji pateikia neigiamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbb45-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="dbb45-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="dbb45-116">Example</span></span>

<span data-ttu-id="dbb45-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` pateikia **–1**.</span><span class="sxs-lookup"><span data-stu-id="dbb45-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbb45-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dbb45-118">Additional resources</span></span>

[<span data-ttu-id="dbb45-119">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="dbb45-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]