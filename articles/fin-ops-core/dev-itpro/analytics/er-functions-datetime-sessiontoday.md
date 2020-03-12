---
title: ER SESSIONTODAY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SESSIONTODAY funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042276"
---
# <span data-ttu-id="e57b0-103"><a name="SESSIONTODAY">ER SESSIONTODAY funkcija</a></span><span class="sxs-lookup"><span data-stu-id="e57b0-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e57b0-104">`SESSIONTODAY` funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos seanso datą.</span><span class="sxs-lookup"><span data-stu-id="e57b0-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e57b0-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="e57b0-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e57b0-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="e57b0-106">Return values</span></span>

<span data-ttu-id="e57b0-107">*Data*</span><span class="sxs-lookup"><span data-stu-id="e57b0-107">*Date*</span></span>

<span data-ttu-id="e57b0-108">Gauta datos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e57b0-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e57b0-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e57b0-109">Example</span></span>

<span data-ttu-id="e57b0-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.</span><span class="sxs-lookup"><span data-stu-id="e57b0-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e57b0-111">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e57b0-111">Additional resources</span></span>

[<span data-ttu-id="e57b0-112">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="e57b0-112">Date and time functions</span></span>](er-functions-category-datetime.md)
