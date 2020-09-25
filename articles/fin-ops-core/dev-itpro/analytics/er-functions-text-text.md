---
title: TEXT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TEXT elektroninių ataskaitų (ER) funkcija.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743693"
---
# <a name="text-er-function"></a><span data-ttu-id="08033-103">TEXT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="08033-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08033-104">`TEXT` funkcija grąžina nurodytą skaičių kaip *Eilutės* reikšmę, jį konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus.</span><span class="sxs-lookup"><span data-stu-id="08033-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="08033-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="08033-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="08033-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="08033-106">Arguments</span></span>

<span data-ttu-id="08033-107">`number`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="08033-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="08033-108">Skaičius, kuris turi būti konvertuotas į teksto eilutę.</span><span class="sxs-lookup"><span data-stu-id="08033-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="08033-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="08033-109">Return values</span></span>

<span data-ttu-id="08033-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="08033-110">*String*</span></span>

<span data-ttu-id="08033-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="08033-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="08033-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="08033-112">Usage notes</span></span>

<span data-ttu-id="08033-113">*Realiojo skaičiaus* tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</span><span class="sxs-lookup"><span data-stu-id="08033-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="08033-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="08033-114">Example</span></span>

<span data-ttu-id="08033-115">Jei „Microsoft Dynamics 365 Finance“ egzemplioriaus serverio lokalė apibrėžta kaip **EN-US**, `TEXT (NOW ())` grąžina dabartinę Finansų seanso datą, pvz., 2015 m. gruodžio 17 d., kaip teksto eilutę **„2015-12-17 07:59:23“**.</span><span class="sxs-lookup"><span data-stu-id="08033-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="08033-116">`TEXT (1/3)` grąžina **„0,33“**.</span><span class="sxs-lookup"><span data-stu-id="08033-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08033-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="08033-117">Additional resources</span></span>

[<span data-ttu-id="08033-118">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="08033-118">Text functions</span></span>](er-functions-category-text.md)
