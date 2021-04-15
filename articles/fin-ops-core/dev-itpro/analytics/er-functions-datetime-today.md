---
title: ER TODAY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) TODAY funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746752"
---
# <a name="today-er-function"></a><span data-ttu-id="f0e99-103">ER TODAY funkcija</span><span class="sxs-lookup"><span data-stu-id="f0e99-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0e99-104">`TODAY` funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos serverio datą.</span><span class="sxs-lookup"><span data-stu-id="f0e99-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e99-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="f0e99-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="f0e99-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="f0e99-106">Return values</span></span>

<span data-ttu-id="f0e99-107">*Data*</span><span class="sxs-lookup"><span data-stu-id="f0e99-107">*Date*</span></span>

<span data-ttu-id="f0e99-108">Gauta datos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f0e99-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="f0e99-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f0e99-109">Example</span></span>

<span data-ttu-id="f0e99-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` dabartinę programos serverio datą – 2015 m. gruodžio 24 d. – pagal nurodytą pasirinktinį formatą pateikia kaip eilutę **„24-12-2015“**.</span><span class="sxs-lookup"><span data-stu-id="f0e99-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0e99-111">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f0e99-111">Additional resources</span></span>

[<span data-ttu-id="f0e99-112">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="f0e99-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]