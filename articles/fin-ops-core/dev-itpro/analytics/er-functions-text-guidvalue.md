---
title: GUIDVALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GUIDVALUE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746392"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="16ff1-103">GUIDVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="16ff1-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16ff1-104">`GUIDVALUE` funkcija konvertuoja nurodytą *Eilutės* tipo įvestį į duomenų elementą, kurio duomenų tipas *GUID*.</span><span class="sxs-lookup"><span data-stu-id="16ff1-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ff1-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="16ff1-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="16ff1-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="16ff1-106">Arguments</span></span>

<span data-ttu-id="16ff1-107">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="16ff1-107">`input`: *String*</span></span>

<span data-ttu-id="16ff1-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="16ff1-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="16ff1-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="16ff1-109">Return values</span></span>

<span data-ttu-id="16ff1-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="16ff1-110">*GUID*</span></span>

<span data-ttu-id="16ff1-111">Gaunama globaliai unikalaus identifikatoriaus (GUID) reikšmė.</span><span class="sxs-lookup"><span data-stu-id="16ff1-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="16ff1-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="16ff1-112">Usage notes</span></span>

<span data-ttu-id="16ff1-113">Norėdami atlikti konvertavimą priešinga kryptimi (t. y. nurodytą duomenų tipo *GUID* įvestį konvertuoti į duomenų tipo *Eilutė* duomenų elementą), galite naudotis funkcija [TEXT()](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="16ff1-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="16ff1-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="16ff1-114">Example</span></span>

<span data-ttu-id="16ff1-115">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="16ff1-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="16ff1-116">Duomenų šaltinis **myID**, kuris priklauso tipui *Apskaičiuojamas laukas* ir turi išraišką `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="16ff1-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="16ff1-117">Duomenų šaltinis **Vartotojai**, kuris priklauso tipui *Lentelės įrašai* ir susijęs su lentele „UserInfo“</span><span class="sxs-lookup"><span data-stu-id="16ff1-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="16ff1-118">Tada galite naudoti išraišką, pvz. `FILTER (Users, Users.objectId = myID)`, filtruoti lentelę „UserInfo“ pagal lauką **objectId**, priklausantį duomenų tipui *GUID*.</span><span class="sxs-lookup"><span data-stu-id="16ff1-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16ff1-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="16ff1-119">Additional resources</span></span>

[<span data-ttu-id="16ff1-120">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="16ff1-120">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]