---
title: QRCODE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama QRCODE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: b62ed829202028ca0cbf95a0dbc3460d047ca5a5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682972"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="6e00d-103">QRCODE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="6e00d-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e00d-104">`QRCODE` funkcija grąžina *konteinerio* reikšmę, kuri pateikia nurodytą eilutę dvejetainiu formatu kaip greito atsakymo kodo (QR kodą) atvaizdą.</span><span class="sxs-lookup"><span data-stu-id="6e00d-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e00d-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6e00d-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="6e00d-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6e00d-106">Arguments</span></span>

<span data-ttu-id="6e00d-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6e00d-107">`text`: *String*</span></span>

<span data-ttu-id="6e00d-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="6e00d-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="6e00d-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="6e00d-109">Return values</span></span>

<span data-ttu-id="6e00d-110">*Konteineris*</span><span class="sxs-lookup"><span data-stu-id="6e00d-110">*Container*</span></span>

<span data-ttu-id="6e00d-111">Gautas dvejetainis srautas.</span><span class="sxs-lookup"><span data-stu-id="6e00d-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="6e00d-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6e00d-112">Example</span></span>

<span data-ttu-id="6e00d-113">Galite sukonfigūruoti elektroninių ataskaitų (ER) formatą, kad sugeneruotumėte siunčiamą dokumentą „Microsoft Office“ formatu („Excel“ darbaknygės arba „Word“ dokumentai), naudodami iš anksto nustatytą šabloną.</span><span class="sxs-lookup"><span data-stu-id="6e00d-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="6e00d-114">Šiame šablone gali būti **Paveikslėlio** objektas („Excel“ darbaknygė) arba **Paveikslėlio turinio valdiklis** („Word“ dokumentas) kaip QR kodo atvaizdo vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="6e00d-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="6e00d-115">Jums reikia pridėti prie sukonfigūruoto ER formato **langelio** elementą, kuris bus naudojamas užpildyti šį vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="6e00d-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="6e00d-116">Norėdami nurodyti, kokia informacija bus saugoma QR kodu, turite nustatyti šio **langelio** elemento susiejimą.</span><span class="sxs-lookup"><span data-stu-id="6e00d-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="6e00d-117">Pavyzdžiui, galite sukonfigūruoti tokį susiejimą, kuriame yra ši išraiška:</span><span class="sxs-lookup"><span data-stu-id="6e00d-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="6e00d-118">Kai paleidžiate sukonfigūruotas ER formatą, **LabelText** lauko, priklausančio duomenų šaltiniui **model.ListOfShelfLabels**, teksto reikšmės bus naudojama generuoti QR kodo atvaizdą.</span><span class="sxs-lookup"><span data-stu-id="6e00d-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="6e00d-119">Šis paveikslėlis pakeis QR kodo atvaizdo vietos rezervavimo ženklą dokumento šablone, naudodamas siuntimo dokumento generavimui.</span><span class="sxs-lookup"><span data-stu-id="6e00d-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="6e00d-120">Kai nuskaitomas šis sugeneruoto dokumento vaizdas, jis grąžina tekstą, paimtą iš lauko **LabelText**, priklausančio duomenų šaltiniui **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="6e00d-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="6e00d-121">Daugiau informacijos žr. [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="6e00d-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e00d-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6e00d-122">Additional resources</span></span>

[<span data-ttu-id="6e00d-123">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="6e00d-123">Text functions</span></span>](er-functions-category-text.md)
