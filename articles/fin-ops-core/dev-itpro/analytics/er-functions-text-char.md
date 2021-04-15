---
title: CHAR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CHAR elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a621328817171be7df0622507c84f5c6f6fe90a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746440"
---
# <a name="char-er-function"></a><span data-ttu-id="9c920-103">CHAR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9c920-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c920-104">`CHAR` funkcija grąžina *Eilutės* reikšmę, kuri pateikia vieną simbolį, kurį nurodo nurodytas „Unicode“ numeris.</span><span class="sxs-lookup"><span data-stu-id="9c920-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c920-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="9c920-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="9c920-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9c920-106">Arguments</span></span>

<span data-ttu-id="9c920-107">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="9c920-107">`number`: *Integer*</span></span>

<span data-ttu-id="9c920-108">Skaičius, atitinkantis numatomą vieną simbolį.</span><span class="sxs-lookup"><span data-stu-id="9c920-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c920-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="9c920-109">Return values</span></span>

<span data-ttu-id="9c920-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9c920-110">*String*</span></span>

<span data-ttu-id="9c920-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="9c920-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9c920-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="9c920-112">Usage notes</span></span>

<span data-ttu-id="9c920-113">Šios funkcijos grąžinta eilutė priklauso nuo kodavimo, kuris pasirinktas pirminiame formato **FAILAS** elemente.</span><span class="sxs-lookup"><span data-stu-id="9c920-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="9c920-114">Norėdami matyti palaikomų kodavimų sąrašą, žr. [Kodavimo klasė](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="9c920-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="9c920-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9c920-115">Example</span></span>

<span data-ttu-id="9c920-116">`CHAR (255)` grąžina **„ÿ“**.</span><span class="sxs-lookup"><span data-stu-id="9c920-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c920-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9c920-117">Additional resources</span></span>

[<span data-ttu-id="9c920-118">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="9c920-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]