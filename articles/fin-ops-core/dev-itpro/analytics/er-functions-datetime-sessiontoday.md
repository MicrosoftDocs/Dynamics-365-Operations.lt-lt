---
title: ER SESSIONTODAY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SESSIONTODAY funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e6ad28e642fcfae3cfa2692a4e41b99fae7fc9df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561355"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="ec67e-103">ER SESSIONTODAY funkcija</span><span class="sxs-lookup"><span data-stu-id="ec67e-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec67e-104">`SESSIONTODAY` funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos seanso datą.</span><span class="sxs-lookup"><span data-stu-id="ec67e-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec67e-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="ec67e-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="ec67e-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="ec67e-106">Return values</span></span>

<span data-ttu-id="ec67e-107">*Data*</span><span class="sxs-lookup"><span data-stu-id="ec67e-107">*Date*</span></span>

<span data-ttu-id="ec67e-108">Gauta datos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="ec67e-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="ec67e-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ec67e-109">Example</span></span>

<span data-ttu-id="ec67e-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.</span><span class="sxs-lookup"><span data-stu-id="ec67e-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec67e-111">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ec67e-111">Additional resources</span></span>

[<span data-ttu-id="ec67e-112">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="ec67e-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]