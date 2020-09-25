---
title: ER ENUMERATE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ENUMERATE funkcija.
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
ms.openlocfilehash: e1871ee41267c2c0e8b35007a47c9601079f05d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745254"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="b0232-103">ER ENUMERATE funkcija</span><span class="sxs-lookup"><span data-stu-id="b0232-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0232-104">`ENUMERATE` funkcija pateikia naują tipo *Įrašų sąrašas* reikšmę, sudarytą iš išvardytų nurodyto sąrašo įrašų.</span><span class="sxs-lookup"><span data-stu-id="b0232-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0232-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="b0232-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="b0232-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b0232-106">Arguments</span></span>

<span data-ttu-id="b0232-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="b0232-107">`list`: *Record list*</span></span>

<span data-ttu-id="b0232-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="b0232-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0232-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="b0232-109">Return values</span></span>

<span data-ttu-id="b0232-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="b0232-110">*Record list*</span></span>

<span data-ttu-id="b0232-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b0232-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b0232-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="b0232-112">Usage notes</span></span>

<span data-ttu-id="b0232-113">Pateiktame išvardytų įrašų sąraše rodomi tolesni papildomi elementai.</span><span class="sxs-lookup"><span data-stu-id="b0232-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="b0232-114">Laukų įrašas (komponentas **Reikšmė**)</span><span class="sxs-lookup"><span data-stu-id="b0232-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="b0232-115">dabartinio įrašo indeksą (**Numerio**komponentas).</span><span class="sxs-lookup"><span data-stu-id="b0232-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="b0232-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b0232-116">Example</span></span>

<span data-ttu-id="b0232-117">Tolesnėje iliustracijoje duomenų šaltinis **Išvardytas** sukurtas kaip išvardytas tiekėjo įrašų sąrašas iš duomenų šaltinio **Tiekėjai**, kuris nurodo lentelę VendTable.</span><span class="sxs-lookup"><span data-stu-id="b0232-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="b0232-118">Tolesnėje iliustracijoje parodytas modulio Elektroninės ataskaitos (ER) formatas.</span><span class="sxs-lookup"><span data-stu-id="b0232-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="b0232-119">Šiame formate sukuriami duomenų susiejimai, siekiant generuoti išeigą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="b0232-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="b0232-120">Ši išeiga atskirus tiekėjus pateikia kaip išvardytus mazgus.</span><span class="sxs-lookup"><span data-stu-id="b0232-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="b0232-121">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</span><span class="sxs-lookup"><span data-stu-id="b0232-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="b0232-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b0232-122">Additional resources</span></span>

[<span data-ttu-id="b0232-123">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="b0232-123">List functions</span></span>](er-functions-category-list.md)
