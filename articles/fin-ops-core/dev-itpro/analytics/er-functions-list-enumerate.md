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
ms.openlocfilehash: d34904571ee6de8b36a0840a9470f16858489163
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042149"
---
# <span data-ttu-id="dade2-103"><a name="ENUMERATE">ER ENUMERATE funkcija</a></span><span class="sxs-lookup"><span data-stu-id="dade2-103"><a name="ENUMERATE">ENUMERATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dade2-104">`ENUMERATE` funkcija pateikia naują tipo *Įrašų sąrašas* reikšmę, sudarytą iš išvardytų nurodyto sąrašo įrašų.</span><span class="sxs-lookup"><span data-stu-id="dade2-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="dade2-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="dade2-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="dade2-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="dade2-106">Arguments</span></span>

<span data-ttu-id="dade2-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="dade2-107">`list`: *Record list*</span></span>

<span data-ttu-id="dade2-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="dade2-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="dade2-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="dade2-109">Return values</span></span>

<span data-ttu-id="dade2-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="dade2-110">*Record list*</span></span>

<span data-ttu-id="dade2-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="dade2-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dade2-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="dade2-112">Usage notes</span></span>

<span data-ttu-id="dade2-113">Pateiktame išvardytų įrašų sąraše rodomi tolesni papildomi elementai.</span><span class="sxs-lookup"><span data-stu-id="dade2-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="dade2-114">Laukų įrašas (komponentas **Reikšmė**)</span><span class="sxs-lookup"><span data-stu-id="dade2-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="dade2-115">dabartinio įrašo indeksą (**Numerio**komponentas).</span><span class="sxs-lookup"><span data-stu-id="dade2-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="dade2-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="dade2-116">Example</span></span>

<span data-ttu-id="dade2-117">Tolesnėje iliustracijoje duomenų šaltinis **Išvardytas** sukurtas kaip išvardytas tiekėjo įrašų sąrašas iš duomenų šaltinio **Tiekėjai**, kuris nurodo lentelę VendTable.</span><span class="sxs-lookup"><span data-stu-id="dade2-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="dade2-118">Tolesnėje iliustracijoje parodytas modulio Elektroninės ataskaitos (ER) formatas.</span><span class="sxs-lookup"><span data-stu-id="dade2-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="dade2-119">Šiame formate sukuriami duomenų susiejimai, siekiant generuoti išeigą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="dade2-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="dade2-120">Ši išeiga atskirus tiekėjus pateikia kaip išvardytus mazgus.</span><span class="sxs-lookup"><span data-stu-id="dade2-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="dade2-121">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</span><span class="sxs-lookup"><span data-stu-id="dade2-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="dade2-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dade2-122">Additional resources</span></span>

[<span data-ttu-id="dade2-123">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="dade2-123">List functions</span></span>](er-functions-category-list.md)
