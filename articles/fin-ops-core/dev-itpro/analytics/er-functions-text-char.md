---
title: CHAR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CHAR elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041238"
---
# <span data-ttu-id="a7d5d-103"><a name="CHAR">CHAR ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="a7d5d-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7d5d-104">`CHAR` funkcija grąžina *Eilutės* reikšmę, kuri pateikia vieną simbolį, kurį nurodo nurodytas „Unicode“ numeris.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d5d-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="a7d5d-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="a7d5d-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="a7d5d-106">Arguments</span></span>

<span data-ttu-id="a7d5d-107">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="a7d5d-107">`number`: *Integer*</span></span>

<span data-ttu-id="a7d5d-108">Skaičius, atitinkantis numatomą vieną simbolį.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="a7d5d-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="a7d5d-109">Return values</span></span>

<span data-ttu-id="a7d5d-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="a7d5d-110">*String*</span></span>

<span data-ttu-id="a7d5d-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a7d5d-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="a7d5d-112">Usage notes</span></span>

<span data-ttu-id="a7d5d-113">Šios funkcijos grąžinta eilutė priklauso nuo kodavimo, kuris pasirinktas pirminiame formato **FAILAS** elemente.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="a7d5d-114">Norėdami matyti palaikomų kodavimų sąrašą, žr. [Kodavimo klasė](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="a7d5d-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="a7d5d-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a7d5d-115">Example</span></span>

<span data-ttu-id="a7d5d-116">`CHAR (255)` grąžina **„ÿ“**.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7d5d-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a7d5d-117">Additional resources</span></span>

[<span data-ttu-id="a7d5d-118">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="a7d5d-118">Text functions</span></span>](er-functions-category-text.md)
