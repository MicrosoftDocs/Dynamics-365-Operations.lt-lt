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
ms.openlocfilehash: 62e34628712066d92a244676123ce928a468ea9e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042394"
---
# <span data-ttu-id="d627e-103"><a name="DAYS">DAYS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d627e-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d627e-104">`DAYS` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="d627e-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="d627e-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="d627e-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="d627e-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d627e-106">Arguments</span></span>

<span data-ttu-id="d627e-107">`date 1`: *Data*</span><span class="sxs-lookup"><span data-stu-id="d627e-107">`date 1`: *Date*</span></span>

<span data-ttu-id="d627e-108">Datos reikšmė, nurodanti pradžios datą dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="d627e-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="d627e-109">`date 2`: *Data*</span><span class="sxs-lookup"><span data-stu-id="d627e-109">`date 2`: *Date*</span></span>

<span data-ttu-id="d627e-110">Datos reikšmė, nurodanti pabaigos datą dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="d627e-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="d627e-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="d627e-111">Return values</span></span>

<span data-ttu-id="d627e-112">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="d627e-112">*Integer*</span></span>

<span data-ttu-id="d627e-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="d627e-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d627e-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="d627e-114">Usage notes</span></span>

<span data-ttu-id="d627e-115">Kai pirmoji data yra vėlesnė nei antroji, `DAYS` funkcija pateikia teigiamą reikšmę, kai pirmoji data sutampa su antrąja, ji pateikia **0** (nulį), o, kai pirmoji data yra ankstesnė nei antroji data, ji pateikia neigiamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d627e-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="d627e-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d627e-116">Example</span></span>

<span data-ttu-id="d627e-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` pateikia **–1**.</span><span class="sxs-lookup"><span data-stu-id="d627e-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d627e-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d627e-118">Additional resources</span></span>

[<span data-ttu-id="d627e-119">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="d627e-119">Date and time functions</span></span>](er-functions-category-datetime.md)
