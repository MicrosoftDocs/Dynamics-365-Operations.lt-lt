---
title: ER FORMATELEMENTNAME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FORMATELEMENTNAME funkcija.
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561307"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="9649a-103">ER FORMATELEMENTNAME funkcija</span><span class="sxs-lookup"><span data-stu-id="9649a-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9649a-104">`FORMATELEMENTNAME` funkcija pateikia tipo *Eilutė* reikšmę, nurodančią modulio Elektroninės ataskaitos (ER) dabartinio formato elemento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9649a-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="9649a-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="9649a-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="9649a-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="9649a-106">Return values</span></span>

<span data-ttu-id="9649a-107">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9649a-107">*String*</span></span>

<span data-ttu-id="9649a-108">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="9649a-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9649a-109">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="9649a-109">Usage notes</span></span>

<span data-ttu-id="9649a-110">Šią funkciją galima iškviesti ER reiškiniuose, kurie buvo sukonfigūruoti ER grupės **Tekstas** formato komponento, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, ypatybėms **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="9649a-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="9649a-111">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9649a-111">Example</span></span>

<span data-ttu-id="9649a-112">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="9649a-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9649a-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9649a-113">Additional resources</span></span>

[<span data-ttu-id="9649a-114">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="9649a-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]