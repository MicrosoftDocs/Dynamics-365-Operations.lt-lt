---
title: ER FORMATELEMENTNAME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FORMATELEMENTNAME funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef59bb44a7096f4c095ce37a89558a717748f02e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685332"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="efeae-103">ER FORMATELEMENTNAME funkcija</span><span class="sxs-lookup"><span data-stu-id="efeae-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efeae-104">`FORMATELEMENTNAME` funkcija pateikia tipo *Eilutė* reikšmę, nurodančią modulio Elektroninės ataskaitos (ER) dabartinio formato elemento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="efeae-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="efeae-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="efeae-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="efeae-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="efeae-106">Return values</span></span>

<span data-ttu-id="efeae-107">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="efeae-107">*String*</span></span>

<span data-ttu-id="efeae-108">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="efeae-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="efeae-109">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="efeae-109">Usage notes</span></span>

<span data-ttu-id="efeae-110">Šią funkciją galima iškviesti ER reiškiniuose, kurie buvo sukonfigūruoti ER grupės **Tekstas** formato komponento, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, ypatybėms **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="efeae-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="efeae-111">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="efeae-111">Example</span></span>

<span data-ttu-id="efeae-112">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="efeae-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efeae-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="efeae-113">Additional resources</span></span>

[<span data-ttu-id="efeae-114">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="efeae-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
